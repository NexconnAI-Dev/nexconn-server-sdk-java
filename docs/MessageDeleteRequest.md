

# MessageDeleteRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**fromUserId** | **String** | Sender user ID of the original message that is being deleted. |  |
|**channelType** | **Integer** | Channel type of the original message. Supports &#x60;1&#x60; direct, &#x60;3&#x60; group, &#x60;4&#x60; open channel, &#x60;6&#x60; system, and &#x60;10&#x60; community. |  |
|**channelId** | **String** | Target identifier of the original message. Depending on &#x60;channelType&#x60;, this can be a user ID, group ID, open channel ID, community channel ID, or system target ID. |  |
|**subchannelId** | **String** | Community subchannel ID. Required only when deleting a community-channel message that was sent to a specific subchannel. |  [optional] |
|**messageId** | **String** | Unique message ID to delete. This corresponds to the message UID returned by send or routing services. |  |
|**sentAt** | **Long** | Send timestamp of the original message in milliseconds. Providing it helps the service locate the original message precisely. |  [optional] |
|**isAdmin** | **Integer** | Whether the deletion is performed as an admin operation. &#x60;1&#x60; shows an admin recall indicator and &#x60;0&#x60; performs a normal sender recall. |  [optional] |
|**disablePush** | **Boolean** | Whether to suppress push notifications for the recall event. Not supported for open channels or community channels. |  [optional] |
|**extra** | **String** | Custom extension data carried with the recall operation. Not supported for community channels. |  [optional] |
|**disableUpdateLastMsg** | **Boolean** | Whether to keep the recall operation from updating the channel&#39;s last-message preview. |  [optional] |



