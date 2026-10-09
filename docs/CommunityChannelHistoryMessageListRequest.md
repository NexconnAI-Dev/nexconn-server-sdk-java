

# CommunityChannelHistoryMessageListRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelId** | **String** | Community channel ID. |  |
|**subchannelId** | **String** | Optional community subchannel ID. When omitted, messages from the whole community channel are queried. |  [optional] |
|**userId** | **String** | User ID of the community-channel participant. |  |
|**startAt** | **Long** | Query start timestamp in Unix milliseconds. Must be greater than or equal to &#x60;endAt&#x60;; the range cannot exceed 14 days. |  |
|**endAt** | **Long** | Query end timestamp in Unix milliseconds. Messages are returned in descending timestamp order. |  |
|**pageSize** | **Integer** | Number of messages to return. Must be between 1 and 100. |  [optional] |
|**includeStart** | **Boolean** | Whether to include the message at &#x60;startAt&#x60; when it matches the query boundary. |  |



