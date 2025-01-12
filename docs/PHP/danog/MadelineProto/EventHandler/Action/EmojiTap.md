---
title: "danog\\MadelineProto\\EventHandler\\Action\\EmojiTap: User has clicked on an animated emoji triggering a [reaction, click here for more info »](https://core.telegram.org/api/animated-emojis#emoji-reactions)."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\EventHandler\Action\EmojiTap`
[Back to index](../../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

User has clicked on an animated emoji triggering a [reaction, click here for more info »](https://core.telegram.org/api/animated-emojis#emoji-reactions).  



## Properties
* `$emoticon`: `string` Emoji
* `$id`: `int` Message ID of the animated emoji that was clicked
* `$animation`: `list<array{t: float, i: int}>` t: number of seconds that passed since the previous tap in the array, the first tap uses a value of `0.0`.
i: 1-based index of the randomly chosen animation for the tap (equivalent to the index of a specific emoji-related animation in [stickerPack](https://core.telegram.org/constructor/stickerPack) + 1).

## Method list:
* [`__construct(string $emoticon, ?int $id, array $animation)`](#__construct)
* [`toRawAction(): array`](#toRawAction)

## Methods:
### <a name="__construct"></a> `__construct(string $emoticon, ?int $id, array $animation)`





