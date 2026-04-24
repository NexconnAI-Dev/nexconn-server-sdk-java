

# ChannelMessageHistoryDeleteRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelType** | **Integer** | Channel type. Supports &#x60;1&#x60; direct, &#x60;3&#x60; group, &#x60;4&#x60; open channel, and &#x60;6&#x60; system (&#x60;HistoryCleanInput&#x60;). |  |
|**fromUserId** | **String** | User whose server-side history is operated on. For open channels, this is the operator ID. |  |
|**channelId** | **String** | Target channel ID (&#x60;targetId&#x60; / conversation target). |  |
|**sentAt** | **String** | Optional cutoff (&#x60;msgTimestamp&#x60;). Serialized as string in &#x60;HistoryCleanInput&#x60;. |  [optional] |



