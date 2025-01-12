---
title: getFullInfo
description: getFullInfo parameters, return type and example
redirect_from: /get_full_info.html
grand_parent:
parent: 
---
## Method: getFullInfo  


### Parameters:

| Name     |    Type       |
|----------|---------------|
|id| A username, a bot API chat id, a [Chat](API_docs/types/Chat.html), a [User](API_docs/types/User.html), an [InputPeer](API_docs/types/InputPeer.html), an [InputUser](API_docs/types/InputUser.html), an [InputChannel](API_docs/types/InputChannel.html), a [Peer](API_docs/types/Peer.html), or a [Chat](API_docs/types/Chat.html) object|

### Return type: [FullInfo](FullInfo.html)

### Example ([now fully async!](https://)):


```php
$Chat = $MadelineProto->getFullInfo($id);
```

