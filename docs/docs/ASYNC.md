reject all 

## Usage

What exactly __is__ **async**, you may ask, and how is it better than **threading** or **multiprocessing**?  
Async is a relatively new programming pattern that allows you to easily write **non-blocking** code **as if you were using standard** blocking functions, all **without** the need for complex message exchange systems and synchronization handling for threaded programs, that only add overhead and complexity to your programs, making everything slower and error-prone.  

That's very cool and all, you might think, but how exactly does this __async__ stuff work? Well, as it turns out, it's very easy.  

Instead of writing code like this:  
```php
$file = $MadelineProto->downloadToDir($bigfile, '/tmp/');
```

Write it like **this**:  
```php
$file = $MadelineProto->downloadToDir($bigfile, '/tmp/');
```

But isn't that's the same code?

**Exactly**.  

Starting from [amphp v3](https://amphp.org) and MadelineProto 8, [native PHP fibers](https://www.php.net/manual/en/language.fibers.php) allow concurrent async execution of code without any special `await` or `yield` keywords.

### That's it.

It's really **that** easy.  

This means that you can handle multiple updates, download/upload multiple files all together in one process, as if you were writing normal synchronous code + making everything a lot faster.  

**WARNING**: MadelineProto async is not compatible with pthreads or pcntl, so please uninstall pthreads and do not use `pcntl_fork` in your bot.  

### Async in [event handler](https://docs.madelineproto.xyz/docs/UPDATES.html#event-driven):

```php
class EventHandler extends \danog\MadelineProto\EventHandler
{
    public function onAny($update)
    {
        if (isset($update['message']['out']) && $update['message']['out']) {
            return;
        }
        if (isset($update['message']['media']) && $update['message']['media']['_'] !== 'messageMediaGame') {
            $this->downloadToDir($update, '/tmp');
            $this->messages->sendMedia(['peer' => $update, 'message' => $update['message']['message'], 'media' => $update]);
        }

        $res = json_encode($update, JSON_PRETTY_PRINT);

        $this->sleep(3);

        try {
            $this->sm($update, "<code>$res</code>\nAsynchronously, after 3 seconds");
        } catch (\danog\MadelineProto\RPCErrorException $e) {
            \danog\MadelineProto\Logger::log((string) $e, \danog\MadelineProto\Logger::FATAL_ERROR);
        } catch (\danog\MadelineProto\Exception $e) {
            \danog\MadelineProto\Logger::log((string) $e, \danog\MadelineProto\Logger::FATAL_ERROR);
        }
    }
    public function sm($peer, $message)
    {
        $this->messages->sendMessage(peer: $peer, message: $message, reply_to_msg_id: isset($update['message']['id']) ? $update['message']['id'] : null, parse_mode: 'HTML');
    }
}
```

### Ignored async

```php
\Revolt\EventLoop::queue(fn () => $MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'a'));
\Revolt\EventLoop::queue(fn () => $MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'b'));
```

You can use the above syntax if don't want the request to block, and you don't need the result of the function.  
Note that the order of execution of the function calls will not be guaranteed.  
See [async forking](#async-forking-does-async-green-thread-forking).  

### Combining async operations

There are AMPHP methods can be used to execute multiple async operations simultaneously and wait for the result of all of them, see the [amphp docs](https://amphp.org/amp#combinators) for more info.  

## MadelineProto and AMPHP async APIs

MadelineProto and AMPHP (through Revolt) both provide a lot of async functions: all of MadelineProto's functions are async, for example; and AMPHP provides [multiple packages](https://amphp.org/packages) to work asynchronously with HTTP requests, websockets, databases (HTTP, MySQL, redis, postgres, DNS, sockets and [much more](https://github.com/amphp/))!  

Also, you should read the [AMPHP docs](https://amphp.org/amp): AMPHP provides multiple helper methods for executing actions repeatedly every N seconds in a non-blocking manner, or to defer execution of certain actions (aka async cron).  

You can also use [danog/loop](https://daniil.it/loop) for that.  

### Helper methods

MadelineProto also provides a few generic async helper methods.  

#### Async sleep (does not block the main thread)
```php
$MadelineProto->sleep(3);
```

#### Async readline (does not block the main thread)
```php
$res = $MadelineProto->readLine('Optional prompt');
```

#### Async echo (does not block the main thread)
```php
$MadelineProto->echo('Hello'.PHP_EOL);
```

#### MadelineProto HTTP client

When using amphp's [http-client](https://amphp.org/http-client) to make high-speed asynchronous HTTP requests (downloading files, etc.), use MadelineProto's modified http-client client, instead.  
It automatically supports the socks/HTTP proxies specified in MadelineProto's settings (will use proxies only if the file can't be downloaded normally), and DoH for greater security.  

To use MadelineProto's http-client client, instead of creating an http-client instance:  
```php
$client = \Amp\Http\Client\HttpClientBuilder::buildDefault();
```

Simply get MadelineProto's HTTP client:  
```php
$client = $MadelineProto->getHTTPClient();
```

From here it's like in the [http-client docs](https://amphp.org/http-client).  

MadelineProto also provides a simplified async version of `file_get_contents`:  
```php
$result = $MadelineProto->fileGetContents('https://myurl');
```

#### Async forking (does async green-thread forking)

Useful if you need to start a process in the background.  

```php
\Revolt\EventLoop::queue(fn () => $MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'test'));
```

If the method throws an exception, it will surface out of the event loop, unless it's intercepted by the configured Revolt exception handler ([startAndLoop](https://docs.madelineproto.xyz/docs/UPDATES.html) automatically sets up an exception handler that reports exception to the userbot's admin).  
Also, the method result can't be used: this is usually not good practice, so it's best to use `\Amp\async` instead, which returns a future that will resolve or fail according to the result of the function.  

```php
$future = \Amp\async(fn () => $MadelineProto->messages->sendMessage(peer: 'danogentili', message: 'test'));
// Use $future to register a callback with catch, use it with combinator functions, and much more...
```

#### Multiple async

Multiple concurrent requests can be started [using `\Amp\async`](#async-forking-does-async-green-thread-forking), this will queue bundle all requests in a single container for higher efficiency, if there are no method calls inbetween the `async` calls.

```php
$res1 = async(fn () => $MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'hi 1'));
$res2 = async(fn () => $MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'hi 2'));
$res3 = async(fn () => $MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'hi 3'));

// The await will send all 3 methods in a single container: ['hi 1', 'hi 2', 'hi 3']
[$res1, $res2, $res3] = await([$res1, $res2, $res3]);

$res1 = async(fn () => $MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'hi 1'));

// This non-async call will send request hi 1 and hi 2 direct in a single container: ['hi 1', 'hi 2 direct']
$MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'hi 2 direct');

$res2 = async(fn () => $MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'hi 2'));
$res3 = async(fn () => $MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'hi 3'));

// The await will send the remaining 2 calls in two container: ['hi 2', 'hi 3']
[$res1, $res2, $res3] = await([$res1, $res2, $res3]);
```

This is the preferred way of combining multiple method calls: this way, the MadelineProto async WriteLoop will combine all method calls in one container, making everything WAY faster.  

Note that the execution order of method calls is not guaranteed in this case, unless a `queueId` argument is also provided, in which case it will be guaranteed to be equal to the queueing order (each method call is queued by the `async` call).  

#### Cancellation

All MadelineProto and amphp methods allow cancelling an in-progress operation, by passing an `\Amp\Cancellation` object to the last parameter of any method, see the [amphp](https://amphp.org/amp#cancellation) documentation for more info.  

Example:

```php
use danog\MadelineProto\RemoteUrl;


$deferredCancellation = new \Amp\DeferredCancellation();
$res1 = async(
     $MadelineProto->sendDocument(...),
     peer: '@danogentili',
     file: new RemoteUrl($url),
     cancellation: $deferredCancellation->getCancellation()
);


// Sometime later, if the user decides to /cancel...
$deferredCancellation->cancel();
```

#### Async flock

```php
$unlock = $MadelineProto->flock($filePath, LOCK_SH);
try {
    // ...
} finally {
    $unlock();
}
```

This will asynchronously wait for a lock on `$filePath` (creating it if it doesn't exist).  
The locking mode can be `LOCK_SH` (shared locks), `LOCK_EX` (exclusive locks), as with the PHP `flock` function.  
A third optional parameter can be set, to specify a polling interval in seconds (0.1 by default).  

### Async loop APIs

MadelineProto provides a very useful async loop APIs, for executing operations periodically or on demand.  
It's a more flexible and powerful alternative to AMPHP's [repeat](https://amphp.org/amp/event-loop/api#repeat), allowing dynamically changeable repeat periods, resumes and signaling.  

See [the documentation](https://daniil.it/loop) for more info!

<a href="https://docs.madelineproto.xyz/docs/FAQ.html">Next section</a>