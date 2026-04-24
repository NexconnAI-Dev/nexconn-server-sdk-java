

# SystemChannelMessageSendRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**fromUserId** | **String** | Sender user ID. The sender should have an access token. |  |
|**toUserIds** | **List&lt;String&gt;** | Recipient user IDs. Up to 100 users are supported in a single request. |  |
|**messageType** | **String** | Message type. Supports built-in types and custom types. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. |  |
|**content** | **String** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. |  |
|**pushContent** | **String** | Push notification text for offline recipients. Required for custom or notification messages that need push delivery. |  [optional] |
|**pushData** | **String** | Custom push payload data. Exposed as &#x60;appData&#x60; on iOS and Android. |  [optional] |
|**shouldPersist** | **Integer** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. |  [optional] |
|**contentAvailable** | **Integer** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. |  [optional] |
|**disablePush** | **Boolean** | Whether to suppress push notifications for offline recipients. |  [optional] |
|**pushExt** | **String** | Extended push configuration (JSON string as accepted by &#x60;SystemChannelMsgSendInput&#x60;). |  [optional] |
|**disableUpdateLastMsg** | **Boolean** | Whether to keep this message from updating the system channel&#39;s last-message preview. |  [optional] |



