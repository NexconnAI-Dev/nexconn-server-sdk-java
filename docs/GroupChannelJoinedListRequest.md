

# GroupChannelJoinedListRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**userId** | **String** | User ID whose joined groups should be listed. |  |
|**role** | **Integer** | Role filter. &#x60;0&#x60; all roles, &#x60;1&#x60; regular member, &#x60;2&#x60; admin, &#x60;3&#x60; owner. |  [optional] |
|**pageToken** | **String** | Pagination token returned by the previous request. Omit it for the first page. |  [optional] |
|**pageSize** | **Integer** | Number of groups to return per page. The official default is 50 and the maximum is 100. |  [optional] |
|**order** | **Integer** | Sort order by join time. &#x60;0&#x60; ascending and &#x60;1&#x60; descending. |  [optional] |



