

# GroupChannelCreateRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelId** | **String** | Legacy &#x60;groupId&#x60;. |  |
|**name** | **String** |  |  |
|**owner** | **String** | Group owner user ID. |  |
|**userIds** | **List&lt;String&gt;** | Invited user IDs. The PDF limits this array to 30 users per request. |  [optional] |
|**groupProfile** | **Map&lt;String, Object&gt;** | Group basic profile object. Common keys include &#x60;introduction&#x60;, &#x60;announcement&#x60;, and &#x60;portraitUrl&#x60;. |  [optional] |
|**permissions** | **Map&lt;String, Object&gt;** | Group permission object defined by the source API. |  [optional] |
|**groupExtProfile** | **Map&lt;String, Object&gt;** | Group extra profile object. Keys must start with &#x60;ext_&#x60; according to the PDF. |  [optional] |



