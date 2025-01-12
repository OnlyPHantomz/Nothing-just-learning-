

// In some other file...
$id = $MadelineProto->broadcastCustom(new CustomBroadcastAction($MadelineProto, 'This broadcast is powered by @MadelineProto!'));
```

### Filtering

All broadcast methods allow specifying a custom peer filter:

```php
<?php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

use danog\MadelineProto\API;
use danog\MadelineProto\Broadcast\Filter;

$MadelineProto = new API('bot.madeline');

// Works OK with both bots and userbots
$MadelineProto->start();

// Or, instead of start() you can use botLogin (bots only)
//$MadelineProto->botLogin('1234:token');

// Send messages, showing the "Forwarded from" header
$id = $MadelineProto->broadcastForwardMessages(
    from_peer: 101374607,
    message_ids: [1, 2, 3, 4],
    drop_author: false,
    filter: new Filter(
        allowUsers: true,
        allowBots: false,
        allowGroups: true,
        allowChannels: false,
        blacklist: [], // Optional
        whitelist: null // Optional array, if null all IDs are allowed (equivalent to *)
    )
);
```

### Cancel a broadcast

Use `cancelBroadcast` to a cancel an in-progress broadcast.

```php
$MadelineProto->cancelBroadcast(123);
```

### Get progress

```php
use danog\MadelineProto\Broadcast\Progress;
use danog\MadelineProto\Broadcast\Status;

$progress = $MadelineProto->getBroadcastProgress(123);

if ($progress !== null) {
    assert($progress instanceof Progress);

    $progressStr = (string) $progress;
    echo "Human-readable progress: $progressStr".PHP_EOL;

    // 123
    $broadcastId = $progress->broadcastId;

    // One of Status::GATHERING_PEERS, Status::BROADCASTING, Status::FINISHED, Status::CANCELLED
    $status = $progress->status;

    $pendingCount = $progress->pendingCount;
    $sucessCount = $progress->successCount;
    $sucessCount = $progress->failCount;
}
```

You can use `getBroadcastProgress` to get the progress of a currently running broadcast.
The method returns null if the broadcast doesn't exist, has already completed or was cancelled.  

Use updateBroadcastProgress updates to get real-time progress status without polling, [here's a full example &raquo;](https://github.com/danog/MadelineProto/blob/v8/examples/bot.php).  

<a href="https://docs.madelineproto.xyz/docs/UPDATES.html">Next section</a>