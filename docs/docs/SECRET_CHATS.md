---
title: 
description: "MadelineProtoz"
nav_order:
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---


MadelineProto provides wrappers to work with secret chats.



```php
$secret_chat = $MadelineProto->requestSecretChat($InputUser);
```

[`requestSecretChat`](https://docs.madelineproto.xyz/requestSecretChat.html) requests a secret secret chat to the [InputUser](https://docs.madelineproto.xyz/API_docs/types/InputUser.html), ID, or username specified, and returns the secret chat ID.



[
    'key' 