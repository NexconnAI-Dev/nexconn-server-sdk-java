

# DirectChannelStreamMessageSendRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**fromUserId** | **String** | Sender user ID. The sender should have an access token so push notifications can display sender information correctly. |  |
|**toUserId** | **String** | Recipient user ID. Only a single recipient is supported per stream message. |  |
|**messageType** | **String** | Message type. Fixed value &#x60;RC:StreamMsg&#x60; for stream messages. |  |
|**content** | [**StreamMessageContent**](StreamMessageContent.md) |  |  |
|**isEchoToSender** | **Integer** | Whether to sync the message to the sender&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. |  [optional] |
|**shouldPersist** | **Integer** | Whether to store the message in recipient cloud history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. |  [optional] |
|**metadata** | **Map&lt;String, String&gt;** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. Up to 100 key-value pairs. |  [optional] |
|**disableUpdateLastMsg** | **Boolean** | Whether to keep this message from updating the channel&#39;s last-message preview. |  [optional] |



