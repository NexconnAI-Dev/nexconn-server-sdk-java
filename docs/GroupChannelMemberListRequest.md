

# GroupChannelMemberListRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelId** | **String** | Group channel ID. |  |
|**memberRole** | **Integer** | Member role filter. &#x60;0&#x60; all members, &#x60;1&#x60; regular members, &#x60;2&#x60; admins, &#x60;3&#x60; owner. |  [optional] |
|**pageToken** | **String** | Pagination token returned by the previous request. Omit it for the first page. |  [optional] |
|**pageSize** | **Integer** | Number of members to return per page. The official default is 50 and the maximum is 100. |  [optional] |
|**order** | **Integer** | Sort order by join time. &#x60;0&#x60; ascending and &#x60;1&#x60; descending. |  [optional] |



