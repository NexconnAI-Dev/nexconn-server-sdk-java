

# GroupChannelStreamMessageSendRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**fromUserId** | **String** | Sender user ID. |  |
|**toChannelId** | **String** | Target group channel ID. |  |
|**messageType** | **String** | Message type. Fixed value &#x60;RC:StreamMsg&#x60; for stream messages. |  |
|**content** | [**StreamMessageContent**](StreamMessageContent.md) |  |  |
|**toUserIds** | **List&lt;String&gt;** | Recipient member user IDs for a targeted group message. Up to 10 users. |  [optional] |
|**isEchoToSender** | **Integer** | Whether to sync the message to the sender&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. |  [optional] |
|**shouldPersist** | **Integer** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. |  [optional] |
|**hasMention** | **Integer** | Whether this is an @mention message. Set to &#x60;1&#x60; when &#x60;content&#x60; contains &#x60;mentionedInfo&#x60;. |  [optional] |
|**metadata** | **Map&lt;String, String&gt;** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. Up to 100 key-value pairs. |  [optional] |
|**disableUpdateLastMsg** | **Boolean** | Whether to keep this message from updating the channel&#39;s last-message preview. |  [optional] |



