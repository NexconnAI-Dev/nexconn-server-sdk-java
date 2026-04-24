

# OpenChannelMessageSendRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**fromUserId** | **String** | Sender user ID. |  |
|**toChannelIds** | **List&lt;String&gt;** | Target open channel IDs. Multiple channels are allowed; the official documentation recommends up to 10 IDs per request. |  |
|**messageType** | **String** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. |  |
|**content** | **String** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. |  |
|**shouldPersist** | **Integer** | Whether to store the message in open channel cloud history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. |  [optional] |
|**isEchoToSender** | **Integer** | Whether to sync the sent message to the sender&#39;s client while online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. |  [optional] |
|**priority** | **Integer** | Message priority. &#x60;0&#x60; standard, &#x60;1&#x60; allowlisted, &#x60;2&#x60; high priority, &#x60;3&#x60; low priority. |  [optional] |



