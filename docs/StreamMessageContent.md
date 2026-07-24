

# StreamMessageContent

Stream message content payload.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**content** | **String** | Stream data chunk. Total message size must not exceed 128 KB across all chunks. |  |
|**seq** | **Long** | Sequence number. Must be greater than 0, starting from 1, strictly incrementing and continuous. |  |
|**complete** | **Boolean** | Whether this is the final chunk in the stream. &#x60;true&#x60; marks the end of the stream. |  |
|**completeReason** | **Integer** | Custom completion reason code. Only effective when &#x60;complete&#x60; is &#x60;true&#x60;. |  [optional] |
|**type** | **String** | Stream content type. Supported on the first chunk only. Default: text. Supported values: text, markdown, html. |  [optional] |
|**messageId** | **String** | Stream message unique ID. Not required for the first chunk. Required for subsequent chunks (use the value returned in the first chunk response). |  [optional] |
|**user** | **Map&lt;String, Object&gt;** | Sender user information object. Supported on the first chunk only. |  [optional] |
|**mentionedInfo** | **Map&lt;String, Object&gt;** | @mention information. Supported on the first chunk only. |  [optional] |
|**extra** | **Map&lt;String, Object&gt;** | Extension information. Supported on the first chunk only. |  [optional] |



