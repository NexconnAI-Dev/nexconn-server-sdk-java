

# MessageRecord


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelId** | **String** | Channel identifier of the stored message. |  [optional] |
|**subchannelId** | **String** | Community subchannel ID associated with the stored message, when applicable. |  [optional] |
|**fromUserId** | **String** | Sender user ID of the stored message. |  [optional] |
|**messageId** | **String** | Unique message ID. |  [optional] |
|**sentAt** | **Long** | Message send timestamp in milliseconds. |  [optional] |
|**messageType** | **String** | Message type of the stored message. |  [optional] |
|**content** | **String** | Raw message content payload as stored by the service. |  [optional] |
|**hasMetadata** | **Boolean** | Whether the message has metadata entries attached. |  [optional] |
|**metadata** | [**List&lt;MessageMetadataListItem&gt;**](MessageMetadataListItem.md) | Structured message metadata entries. Omitted when the original metadata is empty or cannot be parsed. |  [optional] |
|**quote** | **String** | Quoted message details as a JSON string containing msgUID, objectName and fromUserId. Omitted for messages without a quote. |  [optional] |



