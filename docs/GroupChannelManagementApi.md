# GroupChannelManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addGroupChannelAdmins**](GroupChannelManagementApi.md#addGroupChannelAdmins) | **POST** /v4/group-channel/admin/add | Add group admins |
| [**addGroupChannelMemberFavorites**](GroupChannelManagementApi.md#addGroupChannelMemberFavorites) | **POST** /v4/group-channel/member/favorites/add | Add favorite group members |
| [**batchGetGroupChannelMembers**](GroupChannelManagementApi.md#batchGetGroupChannelMembers) | **POST** /v4/group-channel/member/batch/get | Get specific group members |
| [**batchGetGroupChannelProfiles**](GroupChannelManagementApi.md#batchGetGroupChannelProfiles) | **POST** /v4/group-channel/profile/list | List group profiles |
| [**createGroupChannel**](GroupChannelManagementApi.md#createGroupChannel) | **POST** /v4/group-channel/create | Create a group |
| [**deleteGroupChannelAlias**](GroupChannelManagementApi.md#deleteGroupChannelAlias) | **POST** /v4/group-channel/alias/delete | Delete group alias |
| [**dismissGroupChannel**](GroupChannelManagementApi.md#dismissGroupChannel) | **POST** /v4/group-channel/dismiss | Dismiss a group |
| [**getGroupChannelAlias**](GroupChannelManagementApi.md#getGroupChannelAlias) | **POST** /v4/group-channel/alias/get | Get group alias |
| [**joinGroupChannel**](GroupChannelManagementApi.md#joinGroupChannel) | **POST** /v4/group-channel/join | Join a group |
| [**kickUserFromAllGroupChannels**](GroupChannelManagementApi.md#kickUserFromAllGroupChannels) | **POST** /v4/group-channel/member/kickout-all | Remove a user from all groups |
| [**listGroupChannelMemberFavorites**](GroupChannelManagementApi.md#listGroupChannelMemberFavorites) | **POST** /v4/group-channel/member/favorites/list | List favorite group members |
| [**listGroupChannelMembers**](GroupChannelManagementApi.md#listGroupChannelMembers) | **POST** /v4/group-channel/member/list | Query group members |
| [**listGroupChannels**](GroupChannelManagementApi.md#listGroupChannels) | **POST** /v4/group-channel/list | List group channels |
| [**listUserJoinedGroupChannels**](GroupChannelManagementApi.md#listUserJoinedGroupChannels) | **POST** /v4/group-channel/joined/list | Query user&#39;s groups |
| [**quitGroupChannel**](GroupChannelManagementApi.md#quitGroupChannel) | **POST** /v4/group-channel/leave | Leave a group |
| [**removeGroupChannelAdmins**](GroupChannelManagementApi.md#removeGroupChannelAdmins) | **POST** /v4/group-channel/admin/remove | Remove group admins |
| [**removeGroupChannelMemberFavorites**](GroupChannelManagementApi.md#removeGroupChannelMemberFavorites) | **POST** /v4/group-channel/member/favorites/remove | Remove favorite group members |
| [**setGroupChannelAlias**](GroupChannelManagementApi.md#setGroupChannelAlias) | **POST** /v4/group-channel/alias/set | Set group alias |
| [**setGroupChannelMember**](GroupChannelManagementApi.md#setGroupChannelMember) | **POST** /v4/group-channel/member/set | Set group member profile |
| [**transferGroupChannelOwner**](GroupChannelManagementApi.md#transferGroupChannelOwner) | **POST** /v4/group-channel/transfer/owner | Transfer group ownership |
| [**updateGroupChannelProfile**](GroupChannelManagementApi.md#updateGroupChannelProfile) | **POST** /v4/group-channel/profile/update | Update group info |


<a id="addGroupChannelAdmins"></a>
# **addGroupChannelAdmins**
> CodeOnlyResponse addGroupChannelAdmins(groupChannelAdminUsersRequest)

Add group admins

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelAdminUsersRequest groupChannelAdminUsersRequest = new GroupChannelAdminUsersRequest(); // GroupChannelAdminUsersRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addGroupChannelAdmins(groupChannelAdminUsersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#addGroupChannelAdmins");
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
| **groupChannelAdminUsersRequest** | [**GroupChannelAdminUsersRequest**](GroupChannelAdminUsersRequest.md)|  | |

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

<a id="addGroupChannelMemberFavorites"></a>
# **addGroupChannelMemberFavorites**
> CodeOnlyResponse addGroupChannelMemberFavorites(groupChannelMemberFavoritesUpdateRequest)

Add favorite group members

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelMemberFavoritesUpdateRequest groupChannelMemberFavoritesUpdateRequest = new GroupChannelMemberFavoritesUpdateRequest(); // GroupChannelMemberFavoritesUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addGroupChannelMemberFavorites(groupChannelMemberFavoritesUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#addGroupChannelMemberFavorites");
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
| **groupChannelMemberFavoritesUpdateRequest** | [**GroupChannelMemberFavoritesUpdateRequest**](GroupChannelMemberFavoritesUpdateRequest.md)|  | |

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

<a id="batchGetGroupChannelMembers"></a>
# **batchGetGroupChannelMembers**
> GroupChannelMemberBatchGetResponse batchGetGroupChannelMembers(groupChannelMemberBatchGetRequest)

Get specific group members

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelMemberBatchGetRequest groupChannelMemberBatchGetRequest = new GroupChannelMemberBatchGetRequest(); // GroupChannelMemberBatchGetRequest | 
    try {
      GroupChannelMemberBatchGetResponse result = apiInstance.batchGetGroupChannelMembers(groupChannelMemberBatchGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#batchGetGroupChannelMembers");
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
| **groupChannelMemberBatchGetRequest** | [**GroupChannelMemberBatchGetRequest**](GroupChannelMemberBatchGetRequest.md)|  | |

### Return type

[**GroupChannelMemberBatchGetResponse**](GroupChannelMemberBatchGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="batchGetGroupChannelProfiles"></a>
# **batchGetGroupChannelProfiles**
> GroupChannelProfileListResponse batchGetGroupChannelProfiles(groupChannelProfileListRequest)

List group profiles

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelProfileListRequest groupChannelProfileListRequest = new GroupChannelProfileListRequest(); // GroupChannelProfileListRequest | 
    try {
      GroupChannelProfileListResponse result = apiInstance.batchGetGroupChannelProfiles(groupChannelProfileListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#batchGetGroupChannelProfiles");
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
| **groupChannelProfileListRequest** | [**GroupChannelProfileListRequest**](GroupChannelProfileListRequest.md)|  | |

### Return type

[**GroupChannelProfileListResponse**](GroupChannelProfileListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="createGroupChannel"></a>
# **createGroupChannel**
> CodeOnlyResponse createGroupChannel(groupChannelCreateRequest)

Create a group

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelCreateRequest groupChannelCreateRequest = new GroupChannelCreateRequest(); // GroupChannelCreateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.createGroupChannel(groupChannelCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#createGroupChannel");
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
| **groupChannelCreateRequest** | [**GroupChannelCreateRequest**](GroupChannelCreateRequest.md)|  | |

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

<a id="deleteGroupChannelAlias"></a>
# **deleteGroupChannelAlias**
> CodeOnlyResponse deleteGroupChannelAlias(groupChannelAliasGetRequest)

Delete group alias

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelAliasGetRequest groupChannelAliasGetRequest = new GroupChannelAliasGetRequest(); // GroupChannelAliasGetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.deleteGroupChannelAlias(groupChannelAliasGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#deleteGroupChannelAlias");
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
| **groupChannelAliasGetRequest** | [**GroupChannelAliasGetRequest**](GroupChannelAliasGetRequest.md)|  | |

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

<a id="dismissGroupChannel"></a>
# **dismissGroupChannel**
> CodeOnlyResponse dismissGroupChannel(groupChannelDismissRequest)

Dismiss a group

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelDismissRequest groupChannelDismissRequest = new GroupChannelDismissRequest(); // GroupChannelDismissRequest | 
    try {
      CodeOnlyResponse result = apiInstance.dismissGroupChannel(groupChannelDismissRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#dismissGroupChannel");
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
| **groupChannelDismissRequest** | [**GroupChannelDismissRequest**](GroupChannelDismissRequest.md)|  | |

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

<a id="getGroupChannelAlias"></a>
# **getGroupChannelAlias**
> GroupChannelAliasGetResponse getGroupChannelAlias(groupChannelAliasGetRequest)

Get group alias

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelAliasGetRequest groupChannelAliasGetRequest = new GroupChannelAliasGetRequest(); // GroupChannelAliasGetRequest | 
    try {
      GroupChannelAliasGetResponse result = apiInstance.getGroupChannelAlias(groupChannelAliasGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#getGroupChannelAlias");
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
| **groupChannelAliasGetRequest** | [**GroupChannelAliasGetRequest**](GroupChannelAliasGetRequest.md)|  | |

### Return type

[**GroupChannelAliasGetResponse**](GroupChannelAliasGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="joinGroupChannel"></a>
# **joinGroupChannel**
> GroupChannelJoinResponse joinGroupChannel(groupChannelJoinRequest)

Join a group

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelJoinRequest groupChannelJoinRequest = new GroupChannelJoinRequest(); // GroupChannelJoinRequest | 
    try {
      GroupChannelJoinResponse result = apiInstance.joinGroupChannel(groupChannelJoinRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#joinGroupChannel");
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
| **groupChannelJoinRequest** | [**GroupChannelJoinRequest**](GroupChannelJoinRequest.md)|  | |

### Return type

[**GroupChannelJoinResponse**](GroupChannelJoinResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="kickUserFromAllGroupChannels"></a>
# **kickUserFromAllGroupChannels**
> CodeOnlyResponse kickUserFromAllGroupChannels(groupChannelKickUserFromAllRequest)

Remove a user from all groups

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelKickUserFromAllRequest groupChannelKickUserFromAllRequest = new GroupChannelKickUserFromAllRequest(); // GroupChannelKickUserFromAllRequest | 
    try {
      CodeOnlyResponse result = apiInstance.kickUserFromAllGroupChannels(groupChannelKickUserFromAllRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#kickUserFromAllGroupChannels");
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
| **groupChannelKickUserFromAllRequest** | [**GroupChannelKickUserFromAllRequest**](GroupChannelKickUserFromAllRequest.md)|  | |

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

<a id="listGroupChannelMemberFavorites"></a>
# **listGroupChannelMemberFavorites**
> GroupChannelMemberFavoritesListResponse listGroupChannelMemberFavorites(groupChannelMemberFavoritesListRequest)

List favorite group members

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelMemberFavoritesListRequest groupChannelMemberFavoritesListRequest = new GroupChannelMemberFavoritesListRequest(); // GroupChannelMemberFavoritesListRequest | 
    try {
      GroupChannelMemberFavoritesListResponse result = apiInstance.listGroupChannelMemberFavorites(groupChannelMemberFavoritesListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#listGroupChannelMemberFavorites");
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
| **groupChannelMemberFavoritesListRequest** | [**GroupChannelMemberFavoritesListRequest**](GroupChannelMemberFavoritesListRequest.md)|  | |

### Return type

[**GroupChannelMemberFavoritesListResponse**](GroupChannelMemberFavoritesListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listGroupChannelMembers"></a>
# **listGroupChannelMembers**
> GroupChannelMemberListResponse listGroupChannelMembers(groupChannelMemberListRequest)

Query group members

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelMemberListRequest groupChannelMemberListRequest = new GroupChannelMemberListRequest(); // GroupChannelMemberListRequest | 
    try {
      GroupChannelMemberListResponse result = apiInstance.listGroupChannelMembers(groupChannelMemberListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#listGroupChannelMembers");
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
| **groupChannelMemberListRequest** | [**GroupChannelMemberListRequest**](GroupChannelMemberListRequest.md)|  | |

### Return type

[**GroupChannelMemberListResponse**](GroupChannelMemberListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listGroupChannels"></a>
# **listGroupChannels**
> GroupChannelListResponse listGroupChannels(groupChannelListRequest)

List group channels

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelListRequest groupChannelListRequest = new GroupChannelListRequest(); // GroupChannelListRequest | 
    try {
      GroupChannelListResponse result = apiInstance.listGroupChannels(groupChannelListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#listGroupChannels");
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
| **groupChannelListRequest** | [**GroupChannelListRequest**](GroupChannelListRequest.md)|  | |

### Return type

[**GroupChannelListResponse**](GroupChannelListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listUserJoinedGroupChannels"></a>
# **listUserJoinedGroupChannels**
> GroupChannelJoinedListResponse listUserJoinedGroupChannels(groupChannelJoinedListRequest)

Query user&#39;s groups

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelJoinedListRequest groupChannelJoinedListRequest = new GroupChannelJoinedListRequest(); // GroupChannelJoinedListRequest | 
    try {
      GroupChannelJoinedListResponse result = apiInstance.listUserJoinedGroupChannels(groupChannelJoinedListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#listUserJoinedGroupChannels");
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
| **groupChannelJoinedListRequest** | [**GroupChannelJoinedListRequest**](GroupChannelJoinedListRequest.md)|  | |

### Return type

[**GroupChannelJoinedListResponse**](GroupChannelJoinedListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="quitGroupChannel"></a>
# **quitGroupChannel**
> CodeOnlyResponse quitGroupChannel(groupChannelQuitRequest)

Leave a group

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelQuitRequest groupChannelQuitRequest = new GroupChannelQuitRequest(); // GroupChannelQuitRequest | 
    try {
      CodeOnlyResponse result = apiInstance.quitGroupChannel(groupChannelQuitRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#quitGroupChannel");
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
| **groupChannelQuitRequest** | [**GroupChannelQuitRequest**](GroupChannelQuitRequest.md)|  | |

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

<a id="removeGroupChannelAdmins"></a>
# **removeGroupChannelAdmins**
> CodeOnlyResponse removeGroupChannelAdmins(groupChannelAdminUsersRequest)

Remove group admins

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelAdminUsersRequest groupChannelAdminUsersRequest = new GroupChannelAdminUsersRequest(); // GroupChannelAdminUsersRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeGroupChannelAdmins(groupChannelAdminUsersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#removeGroupChannelAdmins");
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
| **groupChannelAdminUsersRequest** | [**GroupChannelAdminUsersRequest**](GroupChannelAdminUsersRequest.md)|  | |

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

<a id="removeGroupChannelMemberFavorites"></a>
# **removeGroupChannelMemberFavorites**
> CodeOnlyResponse removeGroupChannelMemberFavorites(groupChannelMemberFavoritesUpdateRequest)

Remove favorite group members

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelMemberFavoritesUpdateRequest groupChannelMemberFavoritesUpdateRequest = new GroupChannelMemberFavoritesUpdateRequest(); // GroupChannelMemberFavoritesUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeGroupChannelMemberFavorites(groupChannelMemberFavoritesUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#removeGroupChannelMemberFavorites");
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
| **groupChannelMemberFavoritesUpdateRequest** | [**GroupChannelMemberFavoritesUpdateRequest**](GroupChannelMemberFavoritesUpdateRequest.md)|  | |

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

<a id="setGroupChannelAlias"></a>
# **setGroupChannelAlias**
> CodeOnlyResponse setGroupChannelAlias(groupChannelAliasSetRequest)

Set group alias

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelAliasSetRequest groupChannelAliasSetRequest = new GroupChannelAliasSetRequest(); // GroupChannelAliasSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setGroupChannelAlias(groupChannelAliasSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#setGroupChannelAlias");
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
| **groupChannelAliasSetRequest** | [**GroupChannelAliasSetRequest**](GroupChannelAliasSetRequest.md)|  | |

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

<a id="setGroupChannelMember"></a>
# **setGroupChannelMember**
> CodeOnlyResponse setGroupChannelMember(groupChannelMemberSetRequest)

Set group member profile

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelMemberSetRequest groupChannelMemberSetRequest = new GroupChannelMemberSetRequest(); // GroupChannelMemberSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setGroupChannelMember(groupChannelMemberSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#setGroupChannelMember");
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
| **groupChannelMemberSetRequest** | [**GroupChannelMemberSetRequest**](GroupChannelMemberSetRequest.md)|  | |

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

<a id="transferGroupChannelOwner"></a>
# **transferGroupChannelOwner**
> CodeOnlyResponse transferGroupChannelOwner(groupChannelTransferOwnerRequest)

Transfer group ownership

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelTransferOwnerRequest groupChannelTransferOwnerRequest = new GroupChannelTransferOwnerRequest(); // GroupChannelTransferOwnerRequest | 
    try {
      CodeOnlyResponse result = apiInstance.transferGroupChannelOwner(groupChannelTransferOwnerRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#transferGroupChannelOwner");
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
| **groupChannelTransferOwnerRequest** | [**GroupChannelTransferOwnerRequest**](GroupChannelTransferOwnerRequest.md)|  | |

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

<a id="updateGroupChannelProfile"></a>
# **updateGroupChannelProfile**
> CodeOnlyResponse updateGroupChannelProfile(groupChannelProfileUpdateRequest)

Update group info

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelManagementApi apiInstance = new GroupChannelManagementApi(defaultClient);
    
    GroupChannelProfileUpdateRequest groupChannelProfileUpdateRequest = new GroupChannelProfileUpdateRequest(); // GroupChannelProfileUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.updateGroupChannelProfile(groupChannelProfileUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelManagementApi#updateGroupChannelProfile");
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
| **groupChannelProfileUpdateRequest** | [**GroupChannelProfileUpdateRequest**](GroupChannelProfileUpdateRequest.md)|  | |

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

