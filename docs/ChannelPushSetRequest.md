

# ChannelPushSetRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelType** | **String** | Session / channel type as a string (&#x60;1&#x60; to &#x60;10&#x60; as accepted by the server). Matches &#x60;ChannelTypeRequestInput&#x60; in the service. |  |
|**requestId** | **String** | User ID whose channel notification setting is updated. |  |
|**channelId** | **String** | Legacy &#x60;targetId&#x60;. |  |
|**subchannelId** | **String** | Legacy &#x60;busChannel&#x60;. Used for community-channel subchannel level settings. |  [optional] |
|**noDisturbLevel** | **Integer** | Do-not-disturb level (required by service validation; range &#x60;-1&#x60; to &#x60;5&#x60;). |  |



