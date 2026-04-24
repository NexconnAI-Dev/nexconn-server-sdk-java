

# GroupChannelProfileItem


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**channelId** | **String** | Group channel ID. |  [optional] |
|**name** | **String** | Group name. |  [optional] |
|**groupProfile** | **Map&lt;String, Object&gt;** | Group basic profile JSON object, such as introduction, announcement, and portrait URL. |  [optional] |
|**groupExtProfile** | **Map&lt;String, Object&gt;** | Extended group profile JSON object. Keys are typically custom fields prefixed with &#x60;ext_&#x60;. |  [optional] |
|**permissions** | **Map&lt;String, Object&gt;** | Group permission settings JSON object, including join, invite, and profile-management permissions. |  [optional] |
|**owner** | **String** | User ID of the current group owner. |  [optional] |
|**createdAt** | **Long** | Timestamp when the group was created. |  [optional] |
|**memberCount** | **Integer** | Current number of group members. |  [optional] |



