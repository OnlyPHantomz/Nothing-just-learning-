---
title: "danog\\MadelineProto\\EventHandler\\Message\\Service\\DialogDeleteMessages: Deleted messages."
description: 
### <a name="
* `$revoke`: `boolean` Whether to delete the message for all participants of the chat.  



### <a name="reply"></a> `reply(string $message, \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $noWebpage = false, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Reply to the message.


Parameters:

* `$message`: ` call this method.  


Parameters:

* `$file`: `(\danog\
Reply a gif.
  
Please use named arguments 

Parameters:

* `$file`: `(\danog\



### <a name="replyVoice"></a> `replyVoice((\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, (integer|null) $ttl = NULL, (integer|null) $duration = NULL, (array|null) $waveform = NULL, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $forceResend = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Reply a voice.
  
Please use named arguments to call this method.  


Parameters:

* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$ttl`: `(integer|null)` Time to live  
* `$duration`: `(integer|null)` Duration of the voice  
* `$waveform`: `(array|null)` Waveform of the voice  
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
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="replyPhoto"></a> `replyPhoto((\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, ?int $ttl = NULL, bool $spoiler = false, (array|null) $replyMarkup = NULL, (integer|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, bool $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, boolean $forceResend = false, \Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Reply a photo.
  
Please use named arguments to call this method.  


Parameters:

* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$ttl`: `?int`   
* `$spoiler`: `bool`   
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
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../../danog/
* `$updateStickersetsOrder`: `boolean` Whether to move used stickersets to top  
* `$forceResend`: `boolean` Whether to forcefully resend the file, even if its type and name are the same.  
* `$cancellation`: `\Amp\Cancellation` Cancellation.  




### <a name="block"></a> `block(): bool`

Adds the user to the blacklist.



### <a name="unblock"></a> `unblock(): bool`

Deletes the user from the blacklist.



### <a name="getStories"></a> `getStories(): list<\danog\MadelineProto\EventHandler\AbstractStory>`

Get user stories.


#### See also: 
* [`\danog\MadelineProto\EventHandler\AbstractStory`: Represents a Telegram Story.](../../../../../danog/MadelineProto/EventHandler/AbstractStory.html)




### <a name="setAction"></a> `setAction(\danog\MadelineProto\EventHandler\Action $action = \danog\MadelineProto\EventHandler\Action\Typing::__set_state(array(]]): bool`

Sends a current user typing event
(see [SendMessageAction](https://docs.madelineproto.xyz/API_docs/types/SendMessageAction.html) for all event types) to a conversation partner or group.  


Parameters:

* `$action`: `\danog\MadelineProto\EventHandler\Action`   


#### See also: 
* [`\danog\MadelineProto\EventHandler\Action`: In-progress actions.](../../../../../danog/MadelineProto/EventHandler/Action.html)




### <a name="read"></a> `read(bool $readAll = false): boolean`

Mark selected message as read.


Parameters:

* `$readAll`: `bool`   


Return value: if set, read all messages in current chat.


### <a name="enableTTL"></a> `enableTTL(int<1, max> $seconds = 86400): \danog\MadelineProto\EventHandler\Message\Service\DialogSetTTL`

Set maximum Time-To-Live of all messages in the specified chat.


Parameters:

* `$seconds`: `int<1, max>` Automatically delete all messages sent in the chat after this many seconds  


#### See also: 
* `max`
* [`\danog\



### <a name="enableAutoTranslate"></a> `enableAutoTranslate(): bool`

Show the [real-time chat translation popup](https://core.telegram.org/api/translation) for a certain chat.



### <a name="disableAutoTranslate"></a> `disableAutoTranslate(): bool`

Hide the [real-time chat translation popup](https://core.telegram.org/api/translation) for a certain chat.



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
