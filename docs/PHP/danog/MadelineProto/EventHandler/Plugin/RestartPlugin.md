 $



### <a name="
* `$media`: `\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|array|string`   
* `$scriptUrl`: `?
### <a name="


### <a name="getHTTPClient"></a> `getHTTPClient(): \Amp\Http\Client\HttpClient`

Get async HTTP client.


#### See also: 
* `\Amp\Http\Client\HttpClient`




### <a name="getHint"></a> `getHint(): string`

Get current password hint.



### <a name="getId"></a> `getId(mixed $id): int`

Get the bot API ID of a peer.


Parameters:

* `$id`: `mixed` Peer  



### <a name="getInfo"></a> `getInfo(mixed $id, \danog\MadelineProto\API::INFO_TYPE_* $type = \danog\MadelineProto\API::INFO_TYPE_ALL): (\$type is \danog\MadelineProto\API::INFO_TYPE_ALL ? array{User?: array, Chat?: array, bot_api_id: int, user_id?: int, chat_id?: int, channel_id?: int, type: string} : ($type is API::INFO_TYPE_TYPE ? string : ($type is \danog\MadelineProto\API::INFO_TYPE_ID ? int : (array{_: string, user_id?: int, access_hash?: int, min?: bool, chat_id?: int, channel_id?: int} | array{_: string, user_id?: int, access_hash?: int, min?: bool} | array{_: string, channel_id: int, access_hash: int, min: bool}))))`

Get info about peer, returns an Info object.
  
If passed a secret chat ID, returns information about the user, not about the secret chat.  
Use getSecretChat to return information about the secret chat.  


Parameters:

* `$id`: `mixed` Peer  
* `$type`: `\danog\MadelineProto\API::INFO_TYPE_*` Whether to generate an Input*, an InputPeer or the full set of constructors  


#### See also: 
* [https://docs.madelineproto.xyz/Info.html](https://docs.madelineproto.xyz/Info.html)
* `\danog\MadelineProto\API::INFO_TYPE_*`




### <a name="getLogger"></a> `getLogger(): \danog\MadelineProto\Logger`

Get logger.


#### See also: 
* [`\danog\MadelineProto\Logger`: Logger class.](../../../../danog/MadelineProto/Logger.html)




### <a name="getMaps"></a> `getMaps(): ?int`

Get current number of memory-mapped regions, UNIX only.



### <a name="getMaxMaps"></a> `getMaxMaps(): ?int`

Get maximum number of memory-mapped regions, UNIX only.
Use testFibers to get the maximum number of fibers on any platform.  



### <a name="getMemoryProfile"></a> `getMemoryProfile(): string`

Get memory profile with memprof.



### <a name="getMethodNamespaces"></a> `getMethodNamespaces(): array`

Get TL namespaces.



### <a name="getMethodsNamespaced"></a> `getMethodsNamespaced(): array`

Get namespaced methods (method => namespace).



### <a name="getMimeFromBuffer"></a> `getMimeFromBuffer(string $buffer): string`

Get mime type from buffer.


Parameters:

* `$buffer`: `string` Buffer  



### <a name="getMimeFromExtension"></a> `getMimeFromExtension(string $extension, string $default): string`

Get mime type from file extension.


Parameters:

* `$extension`: `string` File extension  
* `$default`: `string` Default mime type  



### <a name="getMimeFromFile"></a> `getMimeFromFile(string $file): string`

Get mime type of file.


Parameters:

* `$file`: `string` File  



### <a name="getPlugin"></a> `getPlugin(class-string<T> $class): \danog\MadelineProto\PluginEventHandler|\danog\MadelineProto\Ipc\EventHandlerProxy|null`

Obtain a certain event handler plugin instance.


Parameters:

* `$class`: `class-string<T>` 

return T|null  


#### See also: 
* [`\danog\MadelineProto\PluginEventHandler`: Plugin event handler class.](../../../../danog/MadelineProto/PluginEventHandler.html)
* `\danog\MadelineProto\Ipc\EventHandlerProxy`




### <a name="getPromCounter"></a> `getPromCounter(string $namespace, string $name, string $help, array<string, string> $labels = []): ?\danog\BetterPrometheus\BetterCounter`

Creates and returns a prometheus counter.
  
Returns null if prometheus stats are disabled.  


Parameters:

* `$namespace`: `string`   
* `$name`: `string`   
* `$help`: `string`   
* `$labels`: `array<string, string>`   


#### See also: 
* `\danog\BetterPrometheus\BetterCounter`




### <a name="getPromGauge"></a> `getPromGauge(string $namespace, string $name, string $help, array<string, string> $labels = []): ?\danog\BetterPrometheus\BetterGauge`

Creates and returns a prometheus gauge.
  
Returns null if prometheus stats are disabled.  


Parameters:

* `$namespace`: `string`   
* `$name`: `string`   
* `$help`: `string`   
* `$labels`: `array<string, string>`   


#### See also: 
* `\danog\BetterPrometheus\BetterGauge`




### <a name="getPromHistogram"></a> `getPromHistogram(string $namespace, string $name, string $help, array<string, string> $labels = [], ?non-empty-list<float> $buckets = NULL): ?\danog\BetterPrometheus\BetterHistogram`

Creates and returns a prometheus histogram.
  
Returns null if prometheus stats are disabled.  


Parameters:

* `$namespace`: `string`   
* `$name`: `string`   
* `$help`: `string`   
* `$labels`: `array<string, string>`   
* `$buckets`: `?non-empty-list<float>`   


#### See also: 
* `non-empty-list`
* `\danog\BetterPrometheus\BetterHistogram`




### <a name="getPromSummary"></a> `getPromSummary(string $namespace, string $name, string $help, array<string, string> $labels = [], int $maxAgeSeconds = 600, ?non-empty-list<float> $quantiles = NULL): ?\danog\BetterPrometheus\BetterSummary`

Creates and returns a prometheus summary.
  
Returns null if prometheus stats are disabled.  


Parameters:

* `$namespace`: `string`   
* `$name`: `string`   
* `$help`: `string`   
* `$labels`: `array<string, string>`   
* `$maxAgeSeconds`: `int`   
* `$quantiles`: `?non-empty-list<float>`   


#### See also: 
* `non-empty-list`
* `\danog\BetterPrometheus\BetterSummary`




### <a name="getPropicInfo"></a> `getPropicInfo(mixed $data): ?\danog\MadelineProto\EventHandler\Media\Photo`

Gets info of the propic of a user.


Parameters:

* `$data`: `mixed`   


#### See also: 
* [`\danog\MadelineProto\EventHandler\Media\Photo`: Represents a photo.](../../../../danog/MadelineProto/EventHandler/Media/Photo.html)




### <a name="getPsrLogger"></a> `getPsrLogger(): \Psr\Log\LoggerInterface`

Get PSR logger.


#### See also: 
* `\Psr\Log\LoggerInterface`




### <a name="getPwrChat"></a> `getPwrChat(mixed $id, bool $fullfetch = true): array`

Get full info about peer (including full list of channel members), returns a Chat object.


Parameters:

* `$id`: `mixed` Peer  
* `$fullfetch`: `bool`   


#### See also: 
* [https://docs.madelineproto.xyz/Chat.html](https://docs.madelineproto.xyz/Chat.html)




### <a name="getSecretChat"></a> `getSecretChat((array|int) $chat): \danog\MadelineProto\SecretChats\SecretChat`

Get secret chat.


Parameters:

* `$chat`: `(array|int)` Secret chat ID  


#### See also: 
* [`\danog\MadelineProto\SecretChats\SecretChat`: Represents a secret chat.](../../../../danog/MadelineProto/SecretChats/SecretChat.html)




### <a name="getSecretMessage"></a> `getSecretMessage(integer $chatId, integer $randomId): \danog\MadelineProto\EventHandler\Message\SecretMessage`

Gets a secret chat message.


Parameters:

* `$chatId`: `integer` Secret chat ID.  
* `$randomId`: `integer` Secret chat message ID.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message\SecretMessage`: Represents New encrypted message.](../../../../danog/MadelineProto/EventHandler/Message/SecretMessage.html)




### <a name="getSelf"></a> `getSelf(): array|false`

Get info about the logged-in user, cached.
  
Use fullGetSelf to bypass the cache.  



### <a name="getSessionName"></a> `getSessionName(): string`

Returns the session name.



### <a name="getSettings"></a> `getSettings(): \danog\MadelineProto\Settings`

Return current settings.


#### See also: 
* [`\danog\MadelineProto\Settings`: Settings class used for configuring MadelineProto.](../../../../danog/MadelineProto/Settings.html)




### <a name="getSponsoredMessages"></a> `getSponsoredMessages((int|string|array) $peer): ?array`

Get sponsored messages for channel.
This method will return an array of [sponsored message objects](https://docs.madelineproto.xyz/API_docs/constructors/sponsoredMessage.html).  
  
See [the API documentation](https://core.telegram.org/api/sponsored-messages) for more info on how to handle sponsored messages.  


Parameters:

* `$peer`: `(int|string|array)` Channel ID, or Update, or Message, or Peer.  



### <a name="getStream"></a> `getStream(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream $stream, ?\Amp\Cancellation $cancellation = NULL, ?int $size = NULL): \Amp\ByteStream\ReadableStream`

Provide a stream for a file, URL or amp stream.


Parameters:

* `$stream`: `\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream`   
* `$cancellation`: `?\Amp\Cancellation`   
* `$size`: `?int`   


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* `\Amp\Cancellation`




### <a name="getStreamPipe"></a> `getStreamPipe(): \Amp\ByteStream\Pipe`

Obtains a pipe that can be used to upload a file from a stream.


#### See also: 
* `\Amp\ByteStream\Pipe`




### <a name="getTL"></a> `getTL(): \danog\MadelineProto\TL\TLInterface`

Get TL serializer.


#### See also: 
* [\danog\MadelineProto\TL\TLInterface](../../../../danog/MadelineProto/TL/TLInterface.html)




### <a name="getType"></a> `getType(mixed $id): \danog\MadelineProto\API::PEER_TYPE_*`

Get type of peer.


Parameters:

* `$id`: `mixed` Peer  


#### See also: 
* `\danog\MadelineProto\API::PEER_TYPE_*`




### <a name="getUpdates"></a> `getUpdates(array{offset?: int, limit?: int, timeout?: float} $params = []): list<array{update_id: mixed, update: mixed}>`

Only useful when consuming MadelineProto updates through an API in another language (like Javascript), **absolutely not recommended when directly writing MadelineProto bots**.
  
`getUpdates` will **greatly slow down your bot** if used directly inside of PHP code.  
  
**Only use the [event handler](#async-event-driven) when writing a MadelineProto bot**, because update handling in the **event handler** is completely parallelized and non-blocking.  


Parameters:

* `$params`: `array{offset?: int, limit?: int, timeout?: float}` Params  



### <a name="getWebMessage"></a> `getWebMessage(string $message): string`

Get a message to show to the user when starting the bot.


Parameters:

* `$message`: `string`   



### <a name="getWebWarnings"></a> `getWebWarnings(): string`

Get various warnings to show to the user in the web UI.



### <a name="hasAdmins"></a> `hasAdmins(): bool`

Check if has admins.



### <a name="hasEventHandler"></a> `hasEventHandler(): bool`

Check if an event handler instance is present.



### <a name="hasPlugin"></a> `hasPlugin(class-string<\danog\MadelineProto\EventHandler> $class): bool`

Check if a certain event handler plugin is installed.


Parameters:

* `$class`: `class-string<\danog\MadelineProto\EventHandler>`   


#### See also: 
* [`\danog\MadelineProto\EventHandler`: Event handler.](../../../../danog/MadelineProto/EventHandler.html)




### <a name="hasReportPeers"></a> `hasReportPeers(): bool`

Check if has report peers.



### <a name="hasSecretChat"></a> `hasSecretChat((array|int) $chat): bool`

Check whether secret chat exists.


Parameters:

* `$chat`: `(array|int)` Secret chat ID  



### <a name="htmlEscape"></a> `htmlEscape(string $what): string`

Escape string for MadelineProto's HTML entity converter.


Parameters:

* `$what`: `string` String to escape  



### <a name="htmlToMessageEntities"></a> `htmlToMessageEntities(string $html): \danog\MadelineProto\TextEntities`

Manually convert HTML to a message and a set of entities.
  
NOTE: You don't have to use this method to send HTML messages.  
  
This method is already called automatically by using parse_mode: "HTML" in messages.sendMessage, messages.sendMedia, et cetera...  


Parameters:

* `$html`: `string`   


Return value: Object containing message and entities

#### See also: 
* [https://docs.madelineproto.xyz/API_docs/methods/messages.sendMessage.html#usage-of-parse_mode](https://docs.madelineproto.xyz/API_docs/methods/messages.sendMessage.html#usage-of-parse_mode)
* [`\danog\MadelineProto\TextEntities`: Class that converts HTML or markdown to a message + set of entities.](../../../../danog/MadelineProto/TextEntities.html)




### <a name="importAuthorization"></a> `importAuthorization(array<int, string> $authorization, int $mainDcID): array`

Import authorization.


Parameters:

* `$authorization`: `array<int, string>` Authorization info  
* `$mainDcID`: `int` Main DC ID  



### <a name="inflateStripped"></a> `inflateStripped(string $stripped): string`

Inflate stripped photosize to full JPG payload.


Parameters:

* `$stripped`: `string` Stripped photosize  



### <a name="initSelfRestart"></a> `initSelfRestart(): void`

Initialize self-restart hack.



### <a name="isAltervista"></a> `isAltervista(): bool`

Whether this is altervista.



### <a name="isArrayOrAlike"></a> `isArrayOrAlike(mixed $var): bool`

Check if is array or similar (traversable && countable && arrayAccess).


Parameters:

* `$var`: `mixed` Value to check  



### <a name="isBot"></a> `isBot(mixed $peer): bool`

Check if the specified peer is a bot.


Parameters:

* `$peer`: `mixed`   



### <a name="isForum"></a> `isForum(mixed $peer): bool`

Check if the specified peer is a forum.


Parameters:

* `$peer`: `mixed`   



### <a name="isIpc"></a> `isIpc(): bool`

Whether we're an IPC client instance.



### <a name="isIpcWorker"></a> `isIpcWorker(): bool`

Whether we're an IPC server process (as opposed to an event handler).



### <a name="isPlayPaused"></a> `isPlayPaused(int $id): bool`

Whether the currently playing audio file is paused.


Parameters:

* `$id`: `int`   



### <a name="isPremium"></a> `isPremium(): bool`

Returns whether the current user is a premium user, cached.



### <a name="isSelfBot"></a> `isSelfBot(): bool`

Returns whether the current user is a bot.



### <a name="isSelfUser"></a> `isSelfUser(): bool`

Returns whether the current user is a user.



### <a name="isTestMode"></a> `isTestMode(): boolean`

Whether we're currently connected to the test DCs.



### <a name="logger"></a> `logger(mixed $param, int $level = \danog\MadelineProto\Logger::NOTICE, string $file = ''): void`

Logger.


Parameters:

* `$param`: `mixed` Parameter  
* `$level`: `int` Logging level  
* `$file`: `string` File where the message originated  



### <a name="logout"></a> `logout(): void`

Logout the session.



### <a name="markdownCodeEscape"></a> `markdownCodeEscape(string $what): string`

Escape string for markdown code section.


Parameters:

* `$what`: `string` String to escape  



### <a name="markdownCodeblockEscape"></a> `markdownCodeblockEscape(string $what): string`

Escape string for markdown codeblock.


Parameters:

* `$what`: `string` String to escape  



### <a name="markdownEscape"></a> `markdownEscape(string $what): string`

Escape string for markdown.


Parameters:

* `$what`: `string` String to escape  



### <a name="markdownToMessageEntities"></a> `markdownToMessageEntities(string $markdown): \danog\MadelineProto\TextEntities`

Manually convert markdown to a message and a set of entities.
  
NOTE: You don't have to use this method to send Markdown messages.  
  
This method is already called automatically by using parse_mode: "Markdown" in messages.sendMessage, messages.sendMedia, et cetera...  


Parameters:

* `$markdown`: `string`   


Return value: Object containing message and entities

#### See also: 
* [https://docs.madelineproto.xyz/API_docs/methods/messages.sendMessage.html#usage-of-parse_mode](https://docs.madelineproto.xyz/API_docs/methods/messages.sendMessage.html#usage-of-parse_mode)
* [`\danog\MadelineProto\TextEntities`: Class that converts HTML or markdown to a message + set of entities.](../../../../danog/MadelineProto/TextEntities.html)




### <a name="markdownUrlEscape"></a> `markdownUrlEscape(string $what): string`

Escape string for URL.


Parameters:

* `$what`: `string` String to escape  



### <a name="mbStrSplit"></a> `mbStrSplit(string $text, integer $length): array<string>`

Telegram UTF-8 multibyte split.


Parameters:

* `$text`: `string` Text  
* `$length`: `integer` Length  



### <a name="mbStrlen"></a> `mbStrlen(string $text): int`

Get Telegram UTF-8 length of string.


Parameters:

* `$text`: `string` Text  



### <a name="mbSubstr"></a> `mbSubstr(string $text, integer $offset, (null|int) $length = NULL): string`

Telegram UTF-8 multibyte substring.


Parameters:

* `$text`: `string` Text to substring  
* `$offset`: `integer` Offset  
* `$length`: `(null|int)` Length  



### <a name="openBuffered"></a> `openBuffered(\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\Amp\ByteStream\ReadableStream $stream, ?\Amp\Cancellation $cancellation = NULL): Closure(int): ?string`

Provide a buffered reader for a file, URL or amp stream.


Parameters:

* `$stream`: `\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\Amp\ByteStream\ReadableStream`   
* `$cancellation`: `?\Amp\Cancellation`   


#### See also: 
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* `\Amp\ByteStream\ReadableStream`
* `\Amp\Cancellation`




### <a name="openFileAppendOnly"></a> `openFileAppendOnly(string $path): \Amp\File\File`

Opens a file in append-only mode.


Parameters:

* `$path`: `string` File path.  


#### See also: 
* `\Amp\File\File`




### <a name="packDouble"></a> `packDouble(float $value): string`

Convert double to binary version.


Parameters:

* `$value`: `float` Value to convert  



### <a name="packSignedInt"></a> `packSignedInt(integer $value): string`

Convert integer to base256 signed int.


Parameters:

* `$value`: `integer` Value to convert  



### <a name="packSignedLong"></a> `packSignedLong(int $value): string`

Convert integer to base256 long.


Parameters:

* `$value`: `int` Value to convert  



### <a name="packUnsignedInt"></a> `packUnsignedInt(int $value): string`

Convert value to unsigned base256 int.


Parameters:

* `$value`: `int` Value  



### <a name="pausePlay"></a> `pausePlay(int $id): void`

Pauses playback of the current audio file in the call.


Parameters:

* `$id`: `int`   



### <a name="peerIsset"></a> `peerIsset(mixed $id): bool`

Check if peer is present in internal peer database.


Parameters:

* `$id`: `mixed` Peer  



### <a name="phoneLogin"></a> `phoneLogin(string $number, integer $sms_type = 5): array`

Login as user.


Parameters:

* `$number`: `string` Phone number  
* `$sms_type`: `integer` SMS type  



### <a name="posmod"></a> `posmod(int $a, int $b): int`

Positive modulo
Works just like the % (modulus) operator, only returns always a postive number.  


Parameters:

* `$a`: `int` A  
* `$b`: `int` B  



### <a name="processDownloadServerPing"></a> `processDownloadServerPing(string $path, string $payload): void`

Internal endpoint used by the download server.


Parameters:

* `$path`: `string`   
* `$payload`: `string`   



### <a name="qrLogin"></a> `qrLogin(): ?\danog\MadelineProto\TL\Types\LoginQrCode`

Initiates QR code login.
  
Returns a QR code login helper object, that can be used to render the QR code, display the link directly, wait for login, QR code expiration and much more.  
  
Returns null if we're already logged in, or if we're waiting for a password (use getAuthorization to distinguish between the two cases).  


#### See also: 
* [`\danog\MadelineProto\TL\Types\LoginQrCode`: Represents a login QR code.](../../../../danog/MadelineProto/TL/Types/LoginQrCode.html)




### <a name="random"></a> `random(integer $length): string`

Get secure random string of specified length.


Parameters:

* `$length`: `integer` Length  



### <a name="randomInt"></a> `randomInt(integer $modulus = 0): int`

Get random integer.


Parameters:

* `$modulus`: `integer` Modulus  



### <a name="readLine"></a> `readLine(string $prompt = '', ?\Amp\Cancellation $cancel = NULL): string`

Asynchronously read line.


Parameters:

* `$prompt`: `string` Prompt  
* `$cancel`: `?\Amp\Cancellation`   


#### See also: 
* `\Amp\Cancellation`




### <a name="refreshFullPeerCache"></a> `refreshFullPeerCache(mixed $id): void`

Refresh full peer cache for a certain peer.


Parameters:

* `$id`: `mixed` The peer to refresh  



### <a name="refreshPeerCache"></a> `refreshPeerCache(mixed ...$ids): void`

Refresh peer cache for a certain peer.


Parameters:

* `...$ids`: `mixed`   



### <a name="renderPromStats"></a> `renderPromStats(?\Prometheus\RendererInterface $renderer = NULL): string`

Renders prometheus stats using the specified renderer.
  
By default uses the text renderer.  


Parameters:

* `$renderer`: `?\Prometheus\RendererInterface`   


#### See also: 
* `\Prometheus\RendererInterface`




### <a name="report"></a> `report(string $message, string $parseMode = ''): void`

Report an error to the previously set peer.


Parameters:

* `$message`: `string` Error to report  
* `$parseMode`: `string` Parse mode  



### <a name="reportMemoryProfile"></a> `reportMemoryProfile(): void`

Report memory profile with memprof.



### <a name="requestCall"></a> `requestCall(mixed $user): \danog\MadelineProto\VoIP`

Request VoIP call.


Parameters:

* `$user`: `mixed` User  


#### See also: 
* [`\danog\MadelineProto\VoIP`: This update represents a VoIP Telegram call.](../../../../danog/MadelineProto/VoIP.html)




### <a name="requestSecretChat"></a> `requestSecretChat(mixed $user): int`

Request secret chat.


Parameters:

* `$user`: `mixed` User to start secret chat with  



### <a name="resetUpdateState"></a> `resetUpdateState(): void`

Reset the update state and fetch all updates from the beginning.



### <a name="restart"></a> `restart(): void`

Restart update loop.



### <a name="resumePlay"></a> `resumePlay(int $id): void`

Resumes playback of the current audio file in the call.


Parameters:

* `$id`: `int`   



### <a name="rethrow"></a> `rethrow(Throwable $e): void`

Rethrow exception into event loop.


Parameters:

* `$e`: `Throwable`   


#### See also: 
* `Throwable`




### <a name="rleDecode"></a> `rleDecode(string $string): string`

null-byte RLE decode.


Parameters:

* `$string`: `string` Data to decode  



### <a name="rleEncode"></a> `rleEncode(string $string): string`

null-byte RLE encode.


Parameters:

* `$string`: `string` Data to encode  



### <a name="sendAudio"></a> `sendAudio((integer|string) $peer, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null) $thumb = NULL, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, ?string $mimeType = NULL, (integer|null) $duration = NULL, (string|null) $title = NULL, (string|null) $performer = NULL, ?int $ttl = NULL, (integer|null) $replyToMsgId = NULL, (integer|null) $topMsgId = NULL, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $forceResend = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Sends an audio.
  
Please use named arguments to call this method.  


Parameters:

* `$peer`: `(integer|string)` Destination peer or username.  
* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$thumb`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null)` Optional: Thumbnail to upload  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$mimeType`: `?string`   
* `$duration`: `(integer|null)` Duration of the audio  
* `$title`: `(string|null)` Title of the audio  
* `$performer`: `(string|null)` Performer of the audio  
* `$ttl`: `?int`   
* `$replyToMsgId`: `(integer|null)` ID of message to reply to.  
* `$topMsgId`: `(integer|null)` ID of thread where to send the message.  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|string|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `boolean` Whether to disable forwards for this message.  
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$forceResend`: `boolean` Whether to forcefully resend the file, even if its type and name are the same.  
* `$cancellation`: `?\Amp\Cancellation` Cancellation.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="sendCustomEvent"></a> `sendCustomEvent(mixed $payload): void`

Sends an updateCustomEvent update to the event handler.


Parameters:

* `$payload`: `mixed`   



### <a name="sendDocument"></a> `sendDocument((integer|string) $peer, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null) $thumb = NULL, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, ?string $mimeType = NULL, ?int $ttl = NULL, bool $spoiler = false, (integer|null) $replyToMsgId = NULL, (integer|null) $topMsgId = NULL, (array|null) $replyMarkup = NULL, (integer|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, bool $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, boolean $forceResend = false, \Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Sends a document.
  
Please use named arguments to call this method.  


Parameters:

* `$peer`: `(integer|string)` Destination peer or username.  
* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$thumb`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null)` Optional: Thumbnail to upload  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$mimeType`: `?string`   
* `$ttl`: `?int`   
* `$spoiler`: `bool`   
* `$replyToMsgId`: `(integer|null)` ID of message to reply to.  
* `$topMsgId`: `(integer|null)` ID of thread where to send the message.  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `bool`   
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$updateStickersetsOrder`: `boolean` Whether to move used stickersets to top  
* `$forceResend`: `boolean` Whether to forcefully resend the file, even if its type and name are the same.  
* `$cancellation`: `\Amp\Cancellation` Cancellation.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="sendDocumentPhoto"></a> `sendDocumentPhoto((integer|string) $peer, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, ?int $ttl = NULL, bool $spoiler = false, (integer|null) $replyToMsgId = NULL, (integer|null) $topMsgId = NULL, (array|null) $replyMarkup = NULL, (integer|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, bool $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, boolean $forceResend = false, \Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Sends a photo.
  
Please use named arguments to call this method.  


Parameters:

* `$peer`: `(integer|string)` Destination peer or username.  
* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$ttl`: `?int`   
* `$spoiler`: `bool`   
* `$replyToMsgId`: `(integer|null)` ID of message to reply to.  
* `$topMsgId`: `(integer|null)` ID of thread where to send the message.  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `bool`   
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$updateStickersetsOrder`: `boolean` Whether to move used stickersets to top  
* `$forceResend`: `boolean` Whether to forcefully resend the file, even if its type and name are the same.  
* `$cancellation`: `\Amp\Cancellation` Cancellation.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="sendGif"></a> `sendGif((integer|string) $peer, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null) $thumb = NULL, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, (integer|null) $ttl = NULL, boolean $spoiler = false, ?int $duration = NULL, ?int $width = NULL, ?int $height = NULL, string $thumbSeek = '00:00:01.000', (integer|null) $replyToMsgId = NULL, (integer|null) $topMsgId = NULL, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $forceResend = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Sends a gif.
  
Please use named arguments to call this method.  


Parameters:

* `$peer`: `(integer|string)` Destination peer or username.  
* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$thumb`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null)` Optional: Thumbnail to upload  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$ttl`: `(integer|null)` Time to live  
* `$spoiler`: `boolean` Whether the message is a spoiler  
* `$duration`: `?int`   
* `$width`: `?int`   
* `$height`: `?int`   
* `$thumbSeek`: `string`   
* `$replyToMsgId`: `(integer|null)` ID of message to reply to.  
* `$topMsgId`: `(integer|null)` ID of thread where to send the message.  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|string|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `boolean` Whether to disable forwards for this message.  
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$forceResend`: `boolean` Whether to forcefully resend the file, even if its type and name are the same.  
* `$cancellation`: `?\Amp\Cancellation` Cancellation.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="sendMessage"></a> `sendMessage((integer|string) $peer, string $message, \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, (integer|null) $replyToMsgId = NULL, (integer|null) $topMsgId = NULL, (array|null) $replyMarkup = NULL, (integer|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, bool $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $noWebpage = false, boolean $updateStickersetsOrder = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Sends a message.


Parameters:

* `$peer`: `(integer|string)` Destination peer or username.  
* `$message`: `string` Message to send  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Parse mode  
* `$replyToMsgId`: `(integer|null)` ID of message to reply to.  
* `$topMsgId`: `(integer|null)` ID of thread where to send the message.  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `bool`   
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$noWebpage`: `boolean` Set this flag to disable generation of the webpage preview  
* `$updateStickersetsOrder`: `boolean` Whether to move used stickersets to top  
* `$cancellation`: `?\Amp\Cancellation` Cancellation  


#### See also: 
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)




### <a name="sendMessageToAdmins"></a> `sendMessageToAdmins(string $message, \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, (array|null) $replyMarkup = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, bool $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $noWebpage = false, ?\Amp\Cancellation $cancellation = NULL): list<\danog\MadelineProto\EventHandler\Message>`

Sends a message to all report peers (admins of the bot).


Parameters:

* `$message`: `string` Message to send  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Parse mode  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `bool`   
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$noWebpage`: `boolean` Set this flag to disable generation of the webpage preview  
* `$cancellation`: `?\Amp\Cancellation`   


#### See also: 
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)




### <a name="sendPhoto"></a> `sendPhoto((integer|string) $peer, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, ?int $ttl = NULL, bool $spoiler = false, (integer|null) $replyToMsgId = NULL, (integer|null) $topMsgId = NULL, (array|null) $replyMarkup = NULL, (integer|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, bool $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, boolean $forceResend = false, \Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Sends a photo.
  
Please use named arguments to call this method.  


Parameters:

* `$peer`: `(integer|string)` Destination peer or username.  
* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$ttl`: `?int`   
* `$spoiler`: `bool`   
* `$replyToMsgId`: `(integer|null)` ID of message to reply to.  
* `$topMsgId`: `(integer|null)` ID of thread where to send the message.  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `bool`   
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$updateStickersetsOrder`: `boolean` Whether to move used stickersets to top  
* `$forceResend`: `boolean` Whether to forcefully resend the file, even if its type and name are the same.  
* `$cancellation`: `\Amp\Cancellation` Cancellation.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="sendSticker"></a> `sendSticker((integer|string) $peer, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, string $mimeType, string $emoji = '', array $stickerSet = [  '_' => 'inputStickerSetEmpty',], ?callable $callback = NULL, ?string $fileName = NULL, ?int $ttl = NULL, (integer|null) $replyToMsgId = NULL, (integer|null) $topMsgId = NULL, (array|null) $replyMarkup = NULL, (integer|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, boolean $forceResend = false, \Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Sends a sticker.
  
Please use named arguments to call this method.  


Parameters:

* `$peer`: `(integer|string)` Destination peer or username.  
* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$mimeType`: `string`   
* `$emoji`: `string`   
* `$stickerSet`: `array`   
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$ttl`: `?int`   
* `$replyToMsgId`: `(integer|null)` ID of message to reply to.  
* `$topMsgId`: `(integer|null)` ID of thread where to send the message.  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `boolean` Whether to disable forwards for this message.  
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$updateStickersetsOrder`: `boolean` Whether to move used stickersets to top  
* `$forceResend`: `boolean` Whether to forcefully resend the file, even if its type and name are the same.  
* `$cancellation`: `\Amp\Cancellation` Cancellation.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* `\Amp\Cancellation`




### <a name="sendVideo"></a> `sendVideo((integer|string) $peer, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null) $thumb = NULL, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, string $mimeType = 'video/mp4', (integer|null) $ttl = NULL, boolean $spoiler = false, boolean $roundMessage = false, boolean $supportsStreaming = true, boolean $noSound = false, (integer|null) $duration = NULL, (integer|null) $width = NULL, (integer|null) $height = NULL, string $thumbSeek = '00:00:01.000', (integer|null) $replyToMsgId = NULL, (integer|null) $topMsgId = NULL, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $forceResend = false, bool $updateStickersetsOrder = false, \Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Sends a video.
  
Please use named arguments to call this method.  


Parameters:

* `$peer`: `(integer|string)` Destination peer or username.  
* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$thumb`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null)` Optional: Thumbnail to upload  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$mimeType`: `string`   
* `$ttl`: `(integer|null)` Time to live  
* `$spoiler`: `boolean` Whether the message is a spoiler  
* `$roundMessage`: `boolean` Whether the message should be round  
* `$supportsStreaming`: `boolean` Whether the video supports streaming  
* `$noSound`: `boolean` Whether the video has no sound  
* `$duration`: `(integer|null)` Duration of the video  
* `$width`: `(integer|null)` Width of the video  
* `$height`: `(integer|null)` Height of the video  
* `$thumbSeek`: `string`   
* `$replyToMsgId`: `(integer|null)` ID of message to reply to.  
* `$topMsgId`: `(integer|null)` ID of thread where to send the message.  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|string|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `boolean` Whether to disable forwards for this message.  
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$forceResend`: `boolean` Whether to forcefully resend the file, even if its type and name are the same.  
* `$updateStickersetsOrder`: `bool`   
* `$cancellation`: `\Amp\Cancellation` Cancellation.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="sendVoice"></a> `sendVoice((integer|string) $peer, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, (integer|null) $ttl = NULL, (integer|null) $duration = NULL, (array|null) $waveform = NULL, (integer|null) $replyToMsgId = NULL, (integer|null) $topMsgId = NULL, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $forceResend = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Sends a voice.
  
Please use named arguments to call this method.  


Parameters:

* `$peer`: `(integer|string)` Destination peer or username.  
* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$ttl`: `(integer|null)` Time to live  
* `$duration`: `(integer|null)` Duration of the voice  
* `$waveform`: `(array|null)` Waveform of the voice  
* `$replyToMsgId`: `(integer|null)` ID of message to reply to.  
* `$topMsgId`: `(integer|null)` ID of thread where to send the message.  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|string|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `boolean` Whether to disable forwards for this message.  
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$forceResend`: `boolean` Whether to forcefully resend the file, even if its type and name are the same.  
* `$cancellation`: `?\Amp\Cancellation` Cancellation.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="setNoop"></a> `setNoop(): void`

Set NOOP update handler, ignoring all updates.



### <a name="setReportPeers"></a> `setReportPeers((int|string|array<(int|string)>) $userOrId): void`

Set peer(s) where to send errors occurred in the event loop.


Parameters:

* `$userOrId`: `(int|string|array<(int|string)>)` Username(s) or peer ID(s)  



### <a name="setWebhook"></a> `setWebhook(string $webhookUrl): void`

Set webhook update handler.


Parameters:

* `$webhookUrl`: `string` Webhook URL  



### <a name="skipPlay"></a> `skipPlay(int $id): void`

When called, skips to the next file in the playlist.


Parameters:

* `$id`: `int`   



### <a name="sleep"></a> `sleep(float $time): void`

Asynchronously sleep.


Parameters:

* `$time`: `float` Number of seconds to sleep for  



### <a name="start"></a> `start(): array`

Log in to telegram (via CLI or web).



### <a name="stop"></a> `stop(): void`

Stop update loop.



### <a name="stopPlay"></a> `stopPlay(int $id): void`

Stops playing all files in the call, clears the main and the hold playlist.


Parameters:

* `$id`: `int`   



### <a name="stringToStream"></a> `stringToStream(string $str): \Amp\ByteStream\ReadableBuffer`

Converts a string into an async amphp stream.


Parameters:

* `$str`: `string`   


#### See also: 
* `\Amp\ByteStream\ReadableBuffer`




### <a name="subscribeToUpdates"></a> `subscribeToUpdates(mixed $channel): bool`

Subscribe to event handler updates for a channel/supergroup we're not a member of.


Parameters:

* `$channel`: `mixed` Channel/supergroup to subscribe to  


Return value: False if we were already subscribed


### <a name="tdToMTProto"></a> `tdToMTProto(array $params): array`

Convert TD to MTProto parameters.


Parameters:

* `$params`: `array` Parameters  



### <a name="tdToTdcli"></a> `tdToTdcli(mixed $params): array`

Convert TD parameters to tdcli.


Parameters:

* `$params`: `mixed` Parameters  



### <a name="tdcliToTd"></a> `tdcliToTd(mixed $params, array $key = NULL): array`

Convert tdcli parameters to tdcli.


Parameters:

* `$params`: `mixed` Params  
* `$key`: `array` Key  



### <a name="testFibers"></a> `testFibers(int $fiberCount = 100000): array{maxFibers: int, realMemoryMb: int, maps: ?int, maxMaps: ?int}`

Test fibers.


Parameters:

* `$fiberCount`: `int`   



### <a name="toCamelCase"></a> `toCamelCase(string $input): string`

Convert to camelCase.


Parameters:

* `$input`: `string` String  



### <a name="toSnakeCase"></a> `toSnakeCase(string $input): string`

Convert to snake_case.


Parameters:

* `$input`: `string` String  



### <a name="unpackDouble"></a> `unpackDouble(string $value): float`

Unpack binary double.


Parameters:

* `$value`: `string` Value to unpack  



### <a name="unpackFileId"></a> `unpackFileId(string $fileId): array`

Unpack bot API file ID.


Parameters:

* `$fileId`: `string` Bot API file ID  


Return value: Unpacked file ID


### <a name="unpackSignedInt"></a> `unpackSignedInt(string $value): int`

Unpack base256 signed int.


Parameters:

* `$value`: `string` base256 int  



### <a name="unpackSignedLong"></a> `unpackSignedLong(string $value): int`

Unpack base256 signed long.


Parameters:

* `$value`: `string` base256 long  



### <a name="unpackSignedLongString"></a> `unpackSignedLongString((string|int|array) $value): string`

Unpack base256 signed long to string.


Parameters:

* `$value`: `(string|int|array)` base256 long  



### <a name="unsetEventHandler"></a> `unsetEventHandler(): void`

Unset event handler.



### <a name="update2fa"></a> `update2fa(array{password?: string, new_password?: string, email?: string, hint?: string} $params): void`

Update the 2FA password.
  
The params array can contain password, new_password, email and hint params.  


Parameters:

* `$params`: `array{password?: string, new_password?: string, email?: string, hint?: string}` The params  



### <a name="updateSettings"></a> `updateSettings(\danog\MadelineProto\SettingsAbstract $settings): void`

Parse, update and store settings.


Parameters:

* `$settings`: `\danog\MadelineProto\SettingsAbstract` Settings  


#### See also: 
* `\danog\MadelineProto\SettingsAbstract`




### <a name="upload"></a> `upload((\danog\MadelineProto\FileCallbackInterface|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|string|array|resource) $file, string $fileName = '', callable $cb = NULL, boolean $encrypted = false, ?\Amp\Cancellation $cancellation = NULL): array`

Upload file.


Parameters:

* `$file`: `(\danog\MadelineProto\FileCallbackInterface|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|string|array|resource)` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback  
* `$encrypted`: `boolean` Whether to encrypt file for secret chats  
* `$cancellation`: `?\Amp\Cancellation`   


Return value: InputFile constructor

#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../../../danog/MadelineProto/FileCallbackInterface.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* `resource`
* `\Amp\Cancellation`




### <a name="uploadEncrypted"></a> `uploadEncrypted((\danog\MadelineProto\FileCallbackInterface|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|string|array|resource) $file, string $fileName = '', callable $cb = NULL, ?\Amp\Cancellation $cancellation = NULL): array`

Upload file to secret chat.


Parameters:

* `$file`: `(\danog\MadelineProto\FileCallbackInterface|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|string|array|resource)` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback  
* `$cancellation`: `?\Amp\Cancellation`   


Return value: InputFile constructor

#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../../../danog/MadelineProto/FileCallbackInterface.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `resource`
* `\Amp\Cancellation`




### <a name="uploadFromCallable"></a> `uploadFromCallable(callable(int, int, ?Cancellation): strin) $callable, integer $size = 0, string $mime = 'application/octet-stream', string $fileName = '', callable(float, float, float): voi) $cb = NULL, boolean $seekable = true, boolean $encrypted = false, ?\Amp\Cancellation $cancellation = NULL): array`

Upload file from callable.
  
The callable must accept two parameters: int $offset, int $size  
The callable must return a string with the contest of the file at the specified offset and size.  


Parameters:

* `$callable`: `callable(int, int, ?Cancellation): strin)` Callable (offset, length) => data  
* `$size`: `integer` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable(float, float, float): voi)` Status callback  
* `$seekable`: `boolean` Whether chunks can be fetched out of order  
* `$encrypted`: `boolean` Whether to encrypt file for secret chats  
* `$cancellation`: `?\Amp\Cancellation`   


Return value: InputFile constructor

#### See also: 
* `\Amp\Cancellation`




### <a name="uploadFromStream"></a> `uploadFromStream(mixed $stream, integer $size = 0, string $mime = 'application/octet-stream', string $fileName = '', callable $cb = NULL, boolean $encrypted = false, ?\Amp\Cancellation $cancellation = NULL): array`

Upload file from stream.


Parameters:

* `$stream`: `mixed` PHP resource or AMPHP async stream  
* `$size`: `integer` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback  
* `$encrypted`: `boolean` Whether to encrypt file for secret chats  
* `$cancellation`: `?\Amp\Cancellation`   


Return value: InputFile constructor

#### See also: 
* `\Amp\Cancellation`




### <a name="uploadFromTgfile"></a> `uploadFromTgfile(mixed $media, callable $cb = NULL, boolean $encrypted = false, ?\Amp\Cancellation $cancellation = NULL): array`

Reupload telegram file.


Parameters:

* `$media`: `mixed` Telegram file  
* `$cb`: `callable` Callback  
* `$encrypted`: `boolean` Whether to encrypt file for secret chats  
* `$cancellation`: `?\Amp\Cancellation`   


Return value: InputFile constructor

#### See also: 
* `\Amp\Cancellation`




### <a name="uploadFromUrl"></a> `uploadFromUrl((string|\danog\MadelineProto\FileCallbackInterface) $url, integer $size = 0, string $fileName = '', callable $cb = NULL, boolean $encrypted = false, ?\Amp\Cancellation $cancellation = NULL): array`

Upload file from URL.


Parameters:

* `$url`: `(string|\danog\MadelineProto\FileCallbackInterface)` URL of file  
* `$size`: `integer` Size of file  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback  
* `$encrypted`: `boolean` Whether to encrypt file for secret chats  
* `$cancellation`: `?\Amp\Cancellation`   


Return value: InputFile constructor

#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](../../../../danog/MadelineProto/FileCallbackInterface.html)
* `\Amp\Cancellation`




### <a name="validateEventHandlerClass"></a> `validateEventHandlerClass(class-string<\danog\MadelineProto\EventHandler> $class): list<\danog\MadelineProto\EventHandlerIssue>`

Perform static analysis on a certain event handler class, to make sure it satisfies some performance requirements.


Parameters:

* `$class`: `class-string<\danog\MadelineProto\EventHandler>` Class name  


#### See also: 
* [`\danog\MadelineProto\EventHandler`: Event handler.](../../../../danog/MadelineProto/EventHandler.html)
* [`\danog\MadelineProto\EventHandlerIssue`: Represents an event handler issue.](../../../../danog/MadelineProto/EventHandlerIssue.html)




### <a name="viewSponsoredMessage"></a> `viewSponsoredMessage((int|array) $peer, (string|array{random_id: string}) $message): bool`

Mark sponsored message as read.


Parameters:

* `$peer`: `(int|array)` Channel ID, or Update, or Message, or Peer.  
* `$message`: `(string|array{random_id: string})` Random ID or sponsored message to mark as read.  



### <a name="wrapMedia"></a> `wrapMedia(array $media, bool $protected = false): ?\danog\MadelineProto\EventHandler\Media`

Wrap a media constructor into an abstract Media object.


Parameters:

* `$media`: `array`   
* `$protected`: `bool`   


#### See also: 
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)




### <a name="wrapMessage"></a> `wrapMessage(array $message, bool $scheduled = false): ?\danog\MadelineProto\EventHandler\AbstractMessage`

Wrap a Message constructor into an abstract Message object.


Parameters:

* `$message`: `array`   
* `$scheduled`: `bool`   


#### See also: 
* [`\danog\MadelineProto\EventHandler\AbstractMessage`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/AbstractMessage.html)




### <a name="wrapPin"></a> `wrapPin(array $message): ?\danog\MadelineProto\EventHandler\Pinned`

Wrap a Pin constructor into an abstract Pinned object.


Parameters:

* `$message`: `array`   


#### See also: 
* [`\danog\MadelineProto\EventHandler\Pinned`: Indicates that some messages were pinned/unpinned.](../../../../danog/MadelineProto/EventHandler/Pinned.html)




### <a name="wrapUpdate"></a> `wrapUpdate(array $update): ?\danog\MadelineProto\EventHandler\Update`

Wrap an Update constructor into an abstract Update object.


Parameters:

* `$update`: `array`   


#### See also: 
* [`\danog\MadelineProto\EventHandler\Update`: Represents a generic update.](../../../../danog/MadelineProto/EventHandler/Update.html)




### <a name="initDbProperties"></a> `initDbProperties(\danog\AsyncOrm\Settings $settings, string $tablePrefix): void`

Initialize database properties.


Parameters:

* `$settings`: `\danog\AsyncOrm\Settings`   
* `$tablePrefix`: `string`   


#### See also: 
* `\danog\AsyncOrm\Settings`




### <a name="saveDbProperties"></a> `saveDbProperties(): void`

Save all properties.



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
