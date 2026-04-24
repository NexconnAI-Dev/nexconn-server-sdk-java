

# OpenChannelCreateRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelId** | **String** | Legacy &#x60;chatroomId&#x60;. |  |
|**destroyType** | **Integer** | &#39;0&#39; for inactive-time destroy and &#39;1&#39; for fixed-time destroy. |  [optional] |
|**ttlMinutes** | **Integer** | Legacy &#x60;destroyTime&#x60;. Valid range is 60 to 10080 minutes according to the PDF. |  [optional] |
|**shouldFreeze** | **Boolean** | Whether whole-channel freeze is enabled when the chatroom is created. |  [optional] |
|**allowedSendersList** | **List&lt;String&gt;** | Allowed senders list applied when the chatroom is frozen. |  [optional] |
|**metadataOwnerId** | **String** | Legacy &#x60;entryOwnerId&#x60;. |  [optional] |
|**metadata** | **Map&lt;String, String&gt;** | Legacy &#x60;entryInfo&#x60;. Open-channel metadata key/value pairs. |  [optional] |



