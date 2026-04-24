# UserManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**banUsers**](UserManagementApi.md#banUsers) | **POST** /v4/user/ban | Ban a user |
| [**batchGetUserTags**](UserManagementApi.md#batchGetUserTags) | **POST** /v4/user/tag/batch/get | Get user tags |
| [**batchSetUserTags**](UserManagementApi.md#batchSetUserTags) | **POST** /v4/user/tag/batch/set | Batch set user tags |
| [**expireAccessToken**](UserManagementApi.md#expireAccessToken) | **POST** /v4/auth/access-token/expire | Expire an access token |
| [**getUser**](UserManagementApi.md#getUser) | **POST** /v4/user/get | Get user info |
| [**getUserConnectionStatus**](UserManagementApi.md#getUserConnectionStatus) | **POST** /v4/user/connection-status/get | Check user online status |
| [**issueAccessToken**](UserManagementApi.md#issueAccessToken) | **POST** /v4/auth/access-token/issue | Register a user |
| [**listBannedUsers**](UserManagementApi.md#listBannedUsers) | **POST** /v4/user/ban/list | List banned users |
| [**listChannelTypeMute**](UserManagementApi.md#listChannelTypeMute) | **POST** /v4/channel-type/mute/list | List muted direct channel users |
| [**listSoftDeletedUsers**](UserManagementApi.md#listSoftDeletedUsers) | **POST** /v4/user/soft-deleted/list | Query soft-deleted users |
| [**restoreUsers**](UserManagementApi.md#restoreUsers) | **POST** /v4/user/restore | Restore a user |
| [**setChannelTypeMute**](UserManagementApi.md#setChannelTypeMute) | **POST** /v4/channel-type/mute/set | Mute a user in direct channels |
| [**softDeleteUsers**](UserManagementApi.md#softDeleteUsers) | **POST** /v4/user/soft-delete | Soft-delete a user |
| [**unbanUsers**](UserManagementApi.md#unbanUsers) | **POST** /v4/user/unban | Unban a user |
| [**updateUser**](UserManagementApi.md#updateUser) | **POST** /v4/user/update | Update user info |


<a id="banUsers"></a>
# **banUsers**
> CodeOnlyResponse banUsers(userBanRequest)

Ban a user

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserBanRequest userBanRequest = new UserBanRequest(); // UserBanRequest | 
    try {
      CodeOnlyResponse result = apiInstance.banUsers(userBanRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#banUsers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userBanRequest** | [**UserBanRequest**](UserBanRequest.md)|  | |

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="batchGetUserTags"></a>
# **batchGetUserTags**
> UserTagBatchGetResponse batchGetUserTags(userTagBatchGetRequest)

Get user tags

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserTagBatchGetRequest userTagBatchGetRequest = new UserTagBatchGetRequest(); // UserTagBatchGetRequest | 
    try {
      UserTagBatchGetResponse result = apiInstance.batchGetUserTags(userTagBatchGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#batchGetUserTags");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userTagBatchGetRequest** | [**UserTagBatchGetRequest**](UserTagBatchGetRequest.md)|  | |

### Return type

[**UserTagBatchGetResponse**](UserTagBatchGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="batchSetUserTags"></a>
# **batchSetUserTags**
> CodeOnlyResponse batchSetUserTags(userTagBatchSetRequest)

Batch set user tags

Rate limit: 10/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserTagBatchSetRequest userTagBatchSetRequest = new UserTagBatchSetRequest(); // UserTagBatchSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.batchSetUserTags(userTagBatchSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#batchSetUserTags");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userTagBatchSetRequest** | [**UserTagBatchSetRequest**](UserTagBatchSetRequest.md)|  | |

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="expireAccessToken"></a>
# **expireAccessToken**
> CodeOnlyResponse expireAccessToken(accessTokenExpireRequest)

Expire an access token

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    AccessTokenExpireRequest accessTokenExpireRequest = new AccessTokenExpireRequest(); // AccessTokenExpireRequest | 
    try {
      CodeOnlyResponse result = apiInstance.expireAccessToken(accessTokenExpireRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#expireAccessToken");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accessTokenExpireRequest** | [**AccessTokenExpireRequest**](AccessTokenExpireRequest.md)|  | |

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getUser"></a>
# **getUser**
> UserGetResponse getUser(userGetRequest)

Get user info

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserGetRequest userGetRequest = new UserGetRequest(); // UserGetRequest | 
    try {
      UserGetResponse result = apiInstance.getUser(userGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#getUser");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userGetRequest** | [**UserGetRequest**](UserGetRequest.md)|  | |

### Return type

[**UserGetResponse**](UserGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getUserConnectionStatus"></a>
# **getUserConnectionStatus**
> UserConnectionStatusResponse getUserConnectionStatus(userConnectionStatusRequest)

Check user online status

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserConnectionStatusRequest userConnectionStatusRequest = new UserConnectionStatusRequest(); // UserConnectionStatusRequest | 
    try {
      UserConnectionStatusResponse result = apiInstance.getUserConnectionStatus(userConnectionStatusRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#getUserConnectionStatus");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userConnectionStatusRequest** | [**UserConnectionStatusRequest**](UserConnectionStatusRequest.md)|  | |

### Return type

[**UserConnectionStatusResponse**](UserConnectionStatusResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="issueAccessToken"></a>
# **issueAccessToken**
> AccessTokenIssueResponse issueAccessToken(accessTokenIssueRequest)

Register a user

Rate limit: 200/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    AccessTokenIssueRequest accessTokenIssueRequest = new AccessTokenIssueRequest(); // AccessTokenIssueRequest | 
    try {
      AccessTokenIssueResponse result = apiInstance.issueAccessToken(accessTokenIssueRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#issueAccessToken");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **accessTokenIssueRequest** | [**AccessTokenIssueRequest**](AccessTokenIssueRequest.md)|  | |

### Return type

[**AccessTokenIssueResponse**](AccessTokenIssueResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listBannedUsers"></a>
# **listBannedUsers**
> UserBanListResponse listBannedUsers(userBanListRequest)

List banned users

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserBanListRequest userBanListRequest = new UserBanListRequest(); // UserBanListRequest | 
    try {
      UserBanListResponse result = apiInstance.listBannedUsers(userBanListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#listBannedUsers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userBanListRequest** | [**UserBanListRequest**](UserBanListRequest.md)|  | |

### Return type

[**UserBanListResponse**](UserBanListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listChannelTypeMute"></a>
# **listChannelTypeMute**
> ChannelTypeMuteListResponse listChannelTypeMute(channelTypeMuteListRequest)

List muted direct channel users

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    ChannelTypeMuteListRequest channelTypeMuteListRequest = new ChannelTypeMuteListRequest(); // ChannelTypeMuteListRequest | 
    try {
      ChannelTypeMuteListResponse result = apiInstance.listChannelTypeMute(channelTypeMuteListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#listChannelTypeMute");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **channelTypeMuteListRequest** | [**ChannelTypeMuteListRequest**](ChannelTypeMuteListRequest.md)|  | |

### Return type

[**ChannelTypeMuteListResponse**](ChannelTypeMuteListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listSoftDeletedUsers"></a>
# **listSoftDeletedUsers**
> UserSoftDeletedListResponse listSoftDeletedUsers(userSoftDeletedListRequest)

Query soft-deleted users

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserSoftDeletedListRequest userSoftDeletedListRequest = new UserSoftDeletedListRequest(); // UserSoftDeletedListRequest | 
    try {
      UserSoftDeletedListResponse result = apiInstance.listSoftDeletedUsers(userSoftDeletedListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#listSoftDeletedUsers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userSoftDeletedListRequest** | [**UserSoftDeletedListRequest**](UserSoftDeletedListRequest.md)|  | |

### Return type

[**UserSoftDeletedListResponse**](UserSoftDeletedListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="restoreUsers"></a>
# **restoreUsers**
> UserOperationResponse restoreUsers(userIdsMax100Request)

Restore a user

Rate limit: 100 users/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserIdsMax100Request userIdsMax100Request = new UserIdsMax100Request(); // UserIdsMax100Request | 
    try {
      UserOperationResponse result = apiInstance.restoreUsers(userIdsMax100Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#restoreUsers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userIdsMax100Request** | [**UserIdsMax100Request**](UserIdsMax100Request.md)|  | |

### Return type

[**UserOperationResponse**](UserOperationResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="setChannelTypeMute"></a>
# **setChannelTypeMute**
> CodeOnlyResponse setChannelTypeMute(channelTypeMuteSetRequest)

Mute a user in direct channels

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    ChannelTypeMuteSetRequest channelTypeMuteSetRequest = new ChannelTypeMuteSetRequest(); // ChannelTypeMuteSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setChannelTypeMute(channelTypeMuteSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#setChannelTypeMute");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **channelTypeMuteSetRequest** | [**ChannelTypeMuteSetRequest**](ChannelTypeMuteSetRequest.md)|  | |

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="softDeleteUsers"></a>
# **softDeleteUsers**
> UserOperationResponse softDeleteUsers(userIdsMax100Request)

Soft-delete a user

Rate limit: 100 users/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserIdsMax100Request userIdsMax100Request = new UserIdsMax100Request(); // UserIdsMax100Request | 
    try {
      UserOperationResponse result = apiInstance.softDeleteUsers(userIdsMax100Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#softDeleteUsers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userIdsMax100Request** | [**UserIdsMax100Request**](UserIdsMax100Request.md)|  | |

### Return type

[**UserOperationResponse**](UserOperationResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="unbanUsers"></a>
# **unbanUsers**
> CodeOnlyResponse unbanUsers(userIdsMax20Request)

Unban a user

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserIdsMax20Request userIdsMax20Request = new UserIdsMax20Request(); // UserIdsMax20Request | 
    try {
      CodeOnlyResponse result = apiInstance.unbanUsers(userIdsMax20Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#unbanUsers");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userIdsMax20Request** | [**UserIdsMax20Request**](UserIdsMax20Request.md)|  | |

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="updateUser"></a>
# **updateUser**
> CodeOnlyResponse updateUser(userUpdateRequest)

Update user info

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserManagementApi apiInstance = new UserManagementApi(defaultClient);
    
    UserUpdateRequest userUpdateRequest = new UserUpdateRequest(); // UserUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.updateUser(userUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserManagementApi#updateUser");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **userUpdateRequest** | [**UserUpdateRequest**](UserUpdateRequest.md)|  | |

### Return type

[**CodeOnlyResponse**](CodeOnlyResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

