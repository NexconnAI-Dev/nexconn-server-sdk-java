

# UserProfileSetRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**userId** | **String** |  |  |
|**userProfile** | **Map&lt;String, Object&gt;** | Basic profile payload. Either &#x60;userProfile&#x60; or &#x60;userExtProfile&#x60; must be provided. |  [optional] |
|**userExtProfile** | **Map&lt;String, String&gt;** | Extended profile payload. Keys are case-sensitive, should use the &#x60;ext_&#x60; prefix, and values must be strings. Either &#x60;userProfile&#x60; or &#x60;userExtProfile&#x60; must be provided.  |  [optional] |



