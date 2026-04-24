

# DirectChannelMessageSendRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**fromUserId** | **String** | Sender user ID. The sender should have an access token so push notifications can display sender information correctly. |  |
|**toUserIds** | **List&lt;String&gt;** | Recipient user IDs. Up to 1000 users are supported in a single request. |  |
|**messageType** | **String** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. |  |
|**content** | **String** | Message content payload. Built-in message types should pass a JSON object serialized as a string. Maximum size is 128 KB. |  |
|**pushContent** | **String** | Push notification text shown to offline recipients. Required for custom message types or notification/signal messages that need push delivery. |  [optional] |
|**pushData** | **String** | Custom payload included in the push notification. Exposed as &#x60;appData&#x60; on iOS and Android. |  [optional] |
|**isEchoToSender** | **Integer** | Whether to sync the message to the sender&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. |  [optional] |
|**count** | **Integer** | Aligns with Java &#x60;DirectChannelMsgSendInput.count&#x60; (push/badge-related counter field name in server model). |  [optional] |
|**verifyBlocklist** | **Integer** | Whether to filter recipients against the sender&#39;s blocklist. &#x60;0&#x60; means no filtering and &#x60;1&#x60; means filter blocked users out. |  [optional] |
|**shouldPersist** | **Integer** | Whether to store the message in recipient cloud history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. |  [optional] |
|**contentAvailable** | **Integer** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. |  [optional] |
|**hasMetadata** | **Boolean** | Whether to enable message metadata (message expansion) for this message. |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. |  [optional] |
|**disablePush** | **Boolean** | Whether to suppress push notifications for offline recipients. |  [optional] |
|**pushExt** | **String** | Extended push configuration (JSON string as accepted by &#x60;DirectChannelMsgSendInput&#x60;). |  [optional] |
|**disableUpdateLastMsg** | **Boolean** | Whether to keep this message from updating the channel&#39;s last-message preview. |  [optional] |
|**needReadReceipt** | **Integer** | Whether to request read receipts for this persisted message. &#x60;1&#x60; requests read receipts and &#x60;0&#x60; disables them. |  [optional] |



