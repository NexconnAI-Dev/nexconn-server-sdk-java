

# MessageMetadataSetRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**messageId** | **String** |  |  |
|**userId** | **String** |  |  |
|**channelType** | **Integer** | Supports &#x60;1&#x60; and &#x60;3&#x60;. |  |
|**channelId** | **String** |  |  |
|**metadata** | **Map&lt;String, String&gt;** | Message metadata to set. Keys support letters, digits, and &#x60;+ &#x3D; - _&#x60;, with a maximum key length of 32 characters. Each request can set up to 100 entries.  |  |
|**isEchoToSender** | **Integer** |  |  [optional] |



