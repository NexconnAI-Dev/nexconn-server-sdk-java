

# GroupChannelTransferOwnerRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelId** | **String** |  |  |
|**newOwner** | **String** |  |  |
|**shouldLeave** | **Integer** | &#x60;0&#x60; means keep the previous owner in the group and &#x60;1&#x60; means leave the group. |  [optional] |
|**shouldDeleteMute** | **Integer** | &#x60;0&#x60; means keep the previous owner&#39;s mute state and &#x60;1&#x60; means remove it. |  [optional] |
|**shouldDeleteAllowedSendersList** | **Integer** | &#x60;0&#x60; means keep the previous owner&#39;s allowed-senders-list state and &#x60;1&#x60; means remove it. |  [optional] |
|**shouldDeleteFavorites** | **Integer** | &#x60;0&#x60; means keep favorites and &#x60;1&#x60; means remove them. |  [optional] |



