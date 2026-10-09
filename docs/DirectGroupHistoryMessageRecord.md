

# DirectGroupHistoryMessageRecord


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelId** | **String** | Channel identifier of the stored message. |  [optional] |
|**fromUserId** | **String** | Sender user ID of the stored message. |  [optional] |
|**messageId** | **String** | Unique message ID. |  [optional] |
|**sentAt** | **Long** | Message send timestamp in milliseconds. |  [optional] |
|**messageType** | **String** | Message type of the stored message. |  [optional] |
|**content** | **String** | Raw message content payload as stored by the service. |  [optional] |
|**hasMetadata** | **Boolean** | Whether the message has metadata entries attached. |  [optional] |
|**metadata** | [**List&lt;MessageMetadataListItem&gt;**](MessageMetadataListItem.md) | Structured message metadata entries. Omitted when the original metadata is empty or cannot be parsed. |  [optional] |
|**aiGenerated** | **Boolean** | Whether the message was AI-generated. Returned only for direct and group channels when the application has enabled this capability. |  [optional] |
|**quote** | **String** | Quoted message details as a JSON string containing msgUID, objectName and fromUserId. Omitted for messages without a quote. |  [optional] |



