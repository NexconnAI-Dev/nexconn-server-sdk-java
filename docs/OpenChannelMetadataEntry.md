

# OpenChannelMetadataEntry


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**key** | **String** |  |  [optional] |
|**value** | **String** |  |  [optional] |
|**metadataOwnerId** | **String** | KV entry owner; serializes as &#x60;metadataOwnerId&#x60; from the source map key &#x60;userId&#x60; (&#x60;OpenChannelMetadataListResult.MetadataItem&#x60;). |  [optional] |
|**shouldAutoDelete** | **Integer** | Parsed from source &#x60;autoDelete&#x60; string. &#x60;1&#x60; enables auto-delete and &#x60;0&#x60; disables it. |  [optional] |
|**updatedAt** | **Long** | Parsed from source &#x60;lastSetTime&#x60; (milliseconds). |  [optional] |



