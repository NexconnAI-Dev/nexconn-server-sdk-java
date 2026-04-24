

# OpenChannelBroadcastRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**fromUserId** | **String** | Sender user ID. |  |
|**messageType** | **String** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. |  |
|**content** | **String** | Broadcast message payload serialized as a string. Maximum size is 128 KB. |  |
|**isEchoToSender** | **Integer** | Whether to sync the broadcast message to the sender&#39;s client while the sender is online. |  [optional] |



