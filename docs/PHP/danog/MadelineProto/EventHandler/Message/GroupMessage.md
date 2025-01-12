---



### <a name="hideHistory"></a> `hideHistory(): void`

Hide message history for new supergroup users.



### <a name="unhideHistory"></a> `unhideHistory(): void`

Unhide message history for new supergroup users.



### <a name="ban"></a> `ban(int $untilDate = 0): void`

Ban message sender from current supergroup.


Parameters:

* `$untilDate`: `int` Validity of said permissions (it is considered forever any value less then 30 seconds or more then 366 days).  



### <a name="unban"></a> `unban(int $untilDate = 0): void`

Unban message sender from current supergroup.


Parameters:

* `$untilDate`: `int` Validity of said permissions (it is considered forever any value less then 30 seconds or more then 366 days).  



### <a name="kick"></a> `kick(): void`

Kick message sender from current supergroup.



### <a name="deleteAll"></a> `deleteAll(bool $forEveryone = true, int $maxId = 0): void`

Delete all supergroup message.


Parameters:

* `$forEveryone`: `bool`   
* `$maxId`: `int`   



### <a name="deleteUserMessages"></a> `deleteUserMessages((string|integer|null) $member = NULL): void`

Delete all messages sent by a specific participant of a given supergroup.


Parameters:

* `$member`: `(string|integer|null)` The participant whose messages should be deleted, if null or absent defaults to the sender of the message.  



### <a name="toSuperGroup"></a> `toSuperGroup(): integer`

Turn a [basic group into a supergroup](https://core.telegram.org/api/channel#migration).


Return value: the channel id we migrated to


### <a name="enableAntiSpam"></a> `enableAntiSpam(): void`

Enable the [native antispam system](https://core.telegram.org/api/antispam).



### <a name="disableAntiSpam"></a> `disableAntiSpam(): void`

Disable the [native antispam system](https://core.telegram.org/api/antispam).



### <a name="enableTopics"></a> `enableTopics(): void`

Enable [forum functionality](https://core.telegram.org/api/forum) in a supergroup.



### <a name="disableTopics"></a> `disableTopics(): void`

Disable [forum functionality](https://core.telegram.org/api/forum) in a supergroup.



### <a name="createTopic"></a> `createTopic(string $title, (\danog\MadelineProto\EventHandler\Topic\IconColor|int) $icon = \danog\MadelineProto\EventHandler\Topic\IconColor::NONE): \danog\MadelineProto\EventHandler\Message\Service\DialogTopicCreated`

Create a [forum topic](https://core.telegram.org/api/forum); requires [`manage_topics` rights](https://core.telegram.org/api/rights).


Parameters:

* `$title`: `string` Topic title (maximum UTF-8 length: 128)  
* `$icon`: `(\danog\MadelineProto\EventHandler\Topic\IconColor|int)` Icon color, or ID of the [custom emoji](https://core.telegram.org/api/custom-emoji) used as topic icon.
                            [Telegram Premium](https://core.telegram.org/api/premium) users can use any custom emoji, other users can only use the custom emojis contained in the [inputStickerSetEmojiDefaultTopicIcons](https://docs.madelineproto.xyz/API_docs/constructors/inputStickerSetEmojiDefaultTopicIcons.html) emoji pack.
                            If no custom emoji icon is specified, specifies the color of the fallback topic icon  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Topic\IconColor`: Specifies the color of the fallback topic icon (RGB) if no custom emoji icon is specified.](../../../../danog/MadelineProto/EventHandler/Topic/IconColor.html)
* [`\danog\MadelineProto\EventHandler\Message\Service\DialogTopicCreated`: A [forum topic](https://core.telegram.org/api/forum#forum-topics) was created.](../../../../danog/MadelineProto/EventHandler/Message/Service/DialogTopicCreated.html)




### <a name="editTopic"></a> `editTopic(string $title, integer $icon = 0, (integer|null) $topicId = NULL): \danog\MadelineProto\EventHandler\Message\Service\DialogTopicEdited`

Edit a [forum topic](https://core.telegram.org/api/forum); requires [`manage_topics` rights](https://core.telegram.org/api/rights).


Parameters:

* `$title`: `string` Topic title (maximum UTF-8 length: 128)  
* `$icon`: `integer` ID of the [custom emoji](https://core.telegram.org/api/custom-emoji) used as topic icon. [Telegram Premium](https://core.telegram.org/api/premium) users can use any custom emoji, other users can only use the custom emojis contained in the [inputStickerSetEmojiDefaultTopicIcons](https://docs.madelineproto.xyz/API_docs/constructors/inputStickerSetEmojiDefaultTopicIcons.html) emoji pack. Pass 0 to switch to the fallback topic icon.  
* `$topicId`: `(integer|null)` Topic ID, if absent defaults to the topic where this message was sent.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message\Service\DialogTopicEdited`: [Forum topic](https://core.telegram.org/api/forum#forum-topics) information was edited.](../../../../danog/MadelineProto/EventHandler/Message/Service/DialogTopicEdited.html)




### <a name="openTopic"></a> `openTopic((integer|null) $topicId = NULL): \danog\MadelineProto\EventHandler\Message\Service\DialogTopicEdited`

Open a [forum topic](https://core.telegram.org/api/forum); requires [`manage_topics` rights](https://core.telegram.org/api/rights).


Parameters:

* `$topicId`: `(integer|null)` Topic ID, if absent defaults to the topic where this message was sent.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message\Service\DialogTopicEdited`: [Forum topic](https://core.telegram.org/api/forum#forum-topics) information was edited.](../../../../danog/MadelineProto/EventHandler/Message/Service/DialogTopicEdited.html)




### <a name="closeTopic"></a> `closeTopic((integer|null) $topicId = NULL): \danog\MadelineProto\EventHandler\Message\Service\DialogTopicEdited`

Close a [forum topic](https://core.telegram.org/api/forum); requires [`manage_topics` rights](https://core.telegram.org/api/rights).


Parameters:

* `$topicId`: `(integer|null)` Topic ID, if absent defaults to the topic where this message was sent.  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message\Service\DialogTopicEdited`: [Forum topic](https://core.telegram.org/api/forum#forum-topics) information was edited.](../../../../danog/MadelineProto/EventHandler/Message/Service/DialogTopicEdited.html)




### <a name="deleteTopic"></a> `deleteTopic((integer|null) $topicId = NULL): void`

Delete message history of a [forum topic](https://core.telegram.org/api/forum).


Parameters:

* `$topicId`: `(integer|null)` Topic ID, if absent defaults to the topic where this message was sent.  



### <a name="enableSlowMode"></a> `enableSlowMode(integer $seconds): void`

Toggle supergroup slow mode: Users will only be able to send one message every `$seconds` seconds.


Parameters:

* `$seconds`: `integer` Users will only be able to send one message every `$seconds` seconds  



### <a name="disableSlowMode"></a> `disableSlowMode(): void`

Disable supergroup slow mode.



### <a name="enableProtection"></a> `enableProtection(): void`

Enable or disable [content protection](https://telegram.org/blog/protected-content-delete-by-date-and-more) on a chat.



### <a name="disableProtection"></a> `disableProtection(): void`

Enable or disable [content protection](https://telegram.org/blog/protected-content-delete-by-date-and-more) on a chat.



### <a name="enableJoinToComment"></a> `enableJoinToComment(): void`

Enable to all users [should join a discussion group in order to comment on a post »](https://core.telegram.org/api/discussion#requiring-users-to-join-the-group).



### <a name="disableJoinToComment"></a> `disableJoinToComment(): void`

Disable to all users [should join a discussion group in order to comment on a post »](https://core.telegram.org/api/discussion#requiring-users-to-join-the-group).



### <a name="pin"></a> `pin(bool $pmOneside = false, bool $silent = false): void`

Pin a message.


Parameters:

* `$pmOneside`: `bool` Whether the message should only be pinned on the local side of a one-to-one chat  
* `$silent`: `bool` Pin the message silently, without triggering a notification  



### <a name="unpin"></a> `unpin(bool $pmOneside = false, bool $silent = false): ?\danog\MadelineProto\EventHandler\Update`

Unpin a message.


Parameters:

* `$pmOneside`: `bool` Whether the message should only be pinned on the local side of a one-to-one chat  
* `$silent`: `bool` Pin the message silently, without triggering a notification  


#### See also: 
* [`\danog\MadelineProto\EventHandler\Update`: Represents a generic update.](../../../../danog/MadelineProto/EventHandler/Update.html)




### <a name="getOurReactions"></a> `getOurReactions(): list<(string|int)>`

Get our reactions on the message.



### <a name="report"></a> `report(\danog\MadelineProto\EventHandler\Message\ReportReason $reason, string $message): bool`

Report a message in a chat for violation of telegram’s Terms of Service.


Parameters:

* `$reason`: `\danog\MadelineProto\EventHandler\Message\ReportReason` Why are these messages being reported  
* `$message`: `string` Comment for report moderation  


#### See also: 
* [\danog\MadelineProto\EventHandler\Message\ReportReason](../../../../danog/MadelineProto/EventHandler/Message/ReportReason.html)




### <a name="saveContact"></a> `saveContact(string $firstName, (string|null) $lastName = NULL, (string|null) $phoneNumber = NULL, bool $addPhonePrivacyException = false): void`

Save message sender to your account contacts.


Parameters:

* `$firstName`: `string` First name  
* `$lastName`: `(string|null)` Last name  
* `$phoneNumber`: `(string|null)` Telegram ID of the other user  
* `$addPhonePrivacyException`: `bool` Allow the other user to see our phone number?  



### <a name="removeContact"></a> `removeContact(): void`

Remove message sender from your account contacts.



### <a name="inviteToChannel"></a> `inviteToChannel((string|int) $channel): void`

Invite message sender to requested channel.


Parameters:

* `$channel`: `(string|int)` Username, Channel ID  



### <a name="addReaction"></a> `addReaction((string|int) $reaction, bool $big = false, bool $addToRecent = true): list<(string|int)>`

Add reaction to message.


Parameters:

* `$reaction`: `(string|int)` reaction  
* `$big`: `bool` Whether a bigger and longer reaction should be shown  
* `$addToRecent`: `bool` Add this reaction to the recent reactions list.  



### <a name="delReaction"></a> `delReaction((string|int) $reaction): list<(string|int)>`

Delete reaction from message.


Parameters:

* `$reaction`: `(string|int)` string or int Reaction  



### <a name="translate"></a> `translate(string $toLang): string`

Translate text message(for media translate it caption).


Parameters:

* `$toLang`: `string` Two-letter ISO 639-1 language code of the language to which the message is translated  



### <a name="editText"></a> `editText(string $message, \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, (array|null) $replyMarkup = NULL, (int|null) $scheduleDate = NULL, bool $noWebpage = false): \danog\MadelineProto\EventHandler\Message`

Edit message text.


Parameters:

* `$message`: `string` New message  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Whether to parse HTML or Markdown markup in the message  
* `$replyMarkup`: `(array|null)` Reply markup for inline keyboards  
* `$scheduleDate`: `(int|null)` Scheduled message date for scheduled messages  
* `$noWebpage`: `bool` Disable webpage preview  


#### See also: 
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)




### <a name="editReplyMarkup"></a> `editReplyMarkup(array $replyMarkup): \danog\MadelineProto\EventHandler\Message`

Edit message keyboard.


Parameters:

* `$replyMarkup`: `array` Reply markup for inline keyboards  



### <a name="replyOrEdit"></a> `replyOrEdit(string $message, \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, (array|null) $replyMarkup = NULL, (int|null) $scheduleDate = NULL, bool $noWebpage = false): \danog\MadelineProto\EventHandler\Message`

If the message is outgoing, will edit the message's text, otherwise will reply to the message.


Parameters:

* `$message`: `string` New message  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Whether to parse HTML or Markdown markup in the message  
* `$replyMarkup`: `(array|null)` Reply markup for inline keyboards  
* `$scheduleDate`: `(int|null)` Scheduled message date for scheduled messages  
* `$noWebpage`: `bool` Disable webpage preview  


#### See also: 
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)




### <a name="forward"></a> `forward((integer|string) $peer, list<int> $id = [], bool $dropAuthor = false, bool $dropCaption = false, int $topicId = 1, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $score = false, (integer|null) $scheduleDate = NULL, (integer|string|null) $sendAs = NULL): non-empty-list<\danog\MadelineProto\EventHandler\Message>`

Forwards messages by their IDs.


Parameters:

* `$peer`: `(integer|string)` Destination peer  
* `$id`: `list<int>` IDs of messages  
* `$dropAuthor`: `bool` Whether to forward messages without quoting the original author  
* `$dropCaption`: `bool` Whether to strip captions from media  
* `$topicId`: `int` Destination [forum topic](https://core.telegram.org/api/forum#forum-topics)  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `boolean` Only for bots, disallows further re-forwarding and saving of the messages, even if the destination chat doesn’t have [content protection](https://telegram.org/blog/protected-content-delete-by-date-and-more) enabled  
* `$background`: `boolean` Send this message as background message  
* `$score`: `boolean` When forwarding games, whether to include your score in the game  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$sendAs`: `(integer|string|null)` Peer to send the message as.  


#### See also: 
* `non-empty-list`




### <a name="getHTML"></a> `getHTML(bool $allowTelegramTags = false): string`

Get an HTML version of the message.


Parameters:

* `$allowTelegramTags`: `bool` Whether to allow telegram-specific tags like tg-spoiler, tg-emoji, mention links and so on...  



### <a name="isReply"></a> `isReply(): bool`

Check if the current message replies to another message.



### <a name="getReply"></a> `getReply(class-string<T> $class = 'danog\\MadelineProto\\EventHandler\\AbstractMessage'): ?T`

Get replied-to message.
  
May return null if the replied-to message was deleted or if the message does not reply to any other message.  


Parameters:

* `$class`: `class-string<T>` Only return a reply if it is of the specified type, return null otherwise.  



### <a name="delete"></a> `delete(boolean $revoke = true): void`

Delete the message.


Parameters:

* `$revoke`: `boolean` Whether to delete the message for all participants of the chat.  



### <a name="reply"></a> `reply(string $message, \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $noWebpage = false, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Reply to the message.


Parameters:

* `$message`: `string` Message to send  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Parse mode  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|string|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$noWebpage`: `boolean` Set this flag to disable generation of the webpage preview  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `boolean` Only for bots, disallows further re-forwarding and saving of the messages, even if the destination chat doesn’t have [content protection](https://telegram.org/blog/protected-content-delete-by-date-and-more) enabled  
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$updateStickersetsOrder`: `boolean` Whether to move used stickersets to top  
* `$cancellation`: `?\Amp\Cancellation`   


#### See also: 
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)




### <a name="replyDocument"></a> `replyDocument((\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null) $thumb = NULL, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, ?string $mimeType = NULL, ?int $ttl = NULL, bool $spoiler = false, (array|null) $replyMarkup = NULL, (integer|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, bool $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, boolean $forceResend = false, \Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Reply a document.
  
Please use named arguments to call this method.  


Parameters:

* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$thumb`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null)` Optional: Thumbnail to upload  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$mimeType`: `?string`   
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
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="replyVideo"></a> `replyVideo((\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null) $thumb = NULL, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, string $mimeType = 'video/mp4', (integer|null) $ttl = NULL, boolean $spoiler = false, boolean $roundMessage = false, boolean $supportsStreaming = true, boolean $noSound = false, (integer|null) $duration = NULL, (integer|null) $width = NULL, (integer|null) $height = NULL, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $forceResend = false, bool $updateStickersetsOrder = false, \Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Reply a video.
  
Please use named arguments to call this method.  


Parameters:

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




### <a name="replyGif"></a> `replyGif((\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null) $thumb = NULL, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, (integer|null) $ttl = NULL, boolean $spoiler = false, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $forceResend = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Reply a gif.
  
Please use named arguments to call this method.  


Parameters:

* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$thumb`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null)` Optional: Thumbnail to upload  
* `$caption`: `string` Caption of document  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Text parse mode for the caption  
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$ttl`: `(integer|null)` Time to live  
* `$spoiler`: `boolean` Whether the message is a spoiler  
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




### <a name="replyAudio"></a> `replyAudio((\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, (\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream|null) $thumb = NULL, string $caption = '', \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, ?callable $callback = NULL, ?string $fileName = NULL, ?string $mimeType = NULL, (integer|null) $duration = NULL, (string|null) $title = NULL, (string|null) $performer = NULL, ?int $ttl = NULL, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $forceResend = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Reply an audio.
  
Please use named arguments to call this method.  


Parameters:

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
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
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
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)
* [`\danog\MadelineProto\EventHandler\Media`: Represents a generic media.](../../../../danog/MadelineProto/EventHandler/Media.html)
* [`\danog\MadelineProto\LocalFile`: Indicates a local file to upload.](../../../../danog/MadelineProto/LocalFile.html)
* [`\danog\MadelineProto\RemoteUrl`: Indicates a remote URL to upload.](../../../../danog/MadelineProto/RemoteUrl.html)
* [`\danog\MadelineProto\BotApiFileId`: Indicates a bot API file ID to upload using sendDocument, sendPhoto etc...](../../../../danog/MadelineProto/BotApiFileId.html)
* `\Amp\ByteStream\ReadableStream`
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`




### <a name="replySticker"></a> `replySticker((\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream) $file, string $mimeType, string $emoji = '', ?callable $callback = NULL, ?string $fileName = NULL, ?int $ttl = NULL, (array|null) $replyMarkup = NULL, (integer|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, boolean $forceResend = false, \Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Reply a sticker.
  
Please use named arguments to call this method.  


Parameters:

* `$file`: `(\danog\MadelineProto\EventHandler\Message|\danog\MadelineProto\EventHandler\Media|\danog\MadelineProto\LocalFile|\danog\MadelineProto\RemoteUrl|\danog\MadelineProto\BotApiFileId|\Amp\ByteStream\ReadableStream)` File to upload: can be a message to reuse media present in a message.  
* `$mimeType`: `string`   
* `$emoji`: `string`   
* `$callback`: `?callable`   
* `$fileName`: `?string` Optional file name, if absent will be extracted from the passed $file.  
* `$ttl`: `?int`   
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




### <a name="sendText"></a> `sendText(string $message, \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, (array|null) $replyMarkup = NULL, (integer|string|null) $sendAs = NULL, (integer|null) $scheduleDate = NULL, boolean $noWebpage = false, boolean $silent = false, boolean $noForwards = false, boolean $background = false, boolean $clearDraft = false, boolean $updateStickersetsOrder = false, ?\Amp\Cancellation $cancellation = NULL): \danog\MadelineProto\EventHandler\Message`

Send a text message.


Parameters:

* `$message`: `string` Message to send  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Parse mode  
* `$replyMarkup`: `(array|null)` Keyboard information.  
* `$sendAs`: `(integer|string|null)` Peer to send the message as.  
* `$scheduleDate`: `(integer|null)` Schedule date.  
* `$noWebpage`: `boolean` Set this flag to disable generation of the webpage preview  
* `$silent`: `boolean` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `boolean` Only for bots, disallows further re-forwarding and saving of the messages, even if the destination chat doesn’t have [content protection](https://telegram.org/blog/protected-content-delete-by-date-and-more) enabled  
* `$background`: `boolean` Send this message as background message  
* `$clearDraft`: `boolean` Clears the draft field  
* `$updateStickersetsOrder`: `boolean` Whether to move used stickersets to top  
* `$cancellation`: `?\Amp\Cancellation`   


#### See also: 
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../danog/MadelineProto/ParseMode.html)
* `\Amp\Cancellation`
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../danog/MadelineProto/EventHandler/Message.html)




### <a name="block"></a> `block(): bool`

Adds the user to the blacklist.



### <a name="unblock"></a> `unblock(): bool`

Deletes the user from the blacklist.



### <a name="getStories"></a> `getStories(): list<\danog\MadelineProto\EventHandler\AbstractStory>`

Get user stories.


#### See also: 
* [`\danog\MadelineProto\EventHandler\AbstractStory`: Represents a Telegram Story.](../../../../danog/MadelineProto/EventHandler/AbstractStory.html)




### <a name="setAction"></a> `setAction(\danog\MadelineProto\EventHandler\Action $action = \danog\MadelineProto\EventHandler\Action\Typing::__set_state(array(]]): bool`

Sends a current user typing event
(see [SendMessageAction](https://docs.madelineproto.xyz/API_docs/types/SendMessageAction.html) for all event types) to a conversation partner or group.  


Parameters:

* `$action`: `\danog\MadelineProto\EventHandler\Action`   


#### See also: 
* [`\danog\MadelineProto\EventHandler\Action`: In-progress actions.](../../../../danog/MadelineProto/EventHandler/Action.html)




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
* [`\danog\MadelineProto\EventHandler\Message\Service\DialogSetTTL`: The Time-To-Live of messages in this chat was changed.](../../../../danog/MadelineProto/EventHandler/Message/Service/DialogSetTTL.html)




### <a name="disableTTL"></a> `disableTTL(): \danog\MadelineProto\EventHandler\Message\Service\DialogSetTTL`

Disable Time-To-Live of all messages in the specified chat.


#### See also: 
* [`\danog\MadelineProto\EventHandler\Message\Service\DialogSetTTL`: The Time-To-Live of messages in this chat was changed.](../../../../danog/MadelineProto/EventHandler/Message/Service/DialogSetTTL.html)




### <a name="enableAutoTranslate"></a> `enableAutoTranslate(): bool`

Show the [real-time chat translation popup](https://core.telegram.org/api/translation) for a certain chat.



### <a name="disableAutoTranslate"></a> `disableAutoTranslate(): bool`

Hide the [real-time chat translation popup](https://core.telegram.org/api/translation) for a certain chat.



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
