# FriendshipApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addFriend**](FriendshipApi.md#addFriend) | **POST** /v4/friend/add | Add friend |
| [**getFriendPermission**](FriendshipApi.md#getFriendPermission) | **POST** /v4/friend/permission/get | Get friend permission |
| [**getFriendRelationships**](FriendshipApi.md#getFriendRelationships) | **POST** /v4/friend/relationship/get | Get friend relationships |
| [**listFriends**](FriendshipApi.md#listFriends) | **POST** /v4/friend/list | List friends |
| [**removeAllFriends**](FriendshipApi.md#removeAllFriends) | **POST** /v4/friend/remove-all | Clean all friends |
| [**removeFriends**](FriendshipApi.md#removeFriends) | **POST** /v4/friend/remove | Delete friends |
| [**setFriendPermission**](FriendshipApi.md#setFriendPermission) | **POST** /v4/friend/permission/set | Set friend permission |
| [**setFriendProfile**](FriendshipApi.md#setFriendProfile) | **POST** /v4/friend/profile/set | Set friend profile |


<a id="addFriend"></a>
# **addFriend**
> CodeOnlyResponse addFriend(friendAddRequest)

Add friend

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.FriendshipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    FriendshipApi apiInstance = new FriendshipApi(defaultClient);
    
    FriendAddRequest friendAddRequest = new FriendAddRequest(); // FriendAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addFriend(friendAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FriendshipApi#addFriend");
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
| **friendAddRequest** | [**FriendAddRequest**](FriendAddRequest.md)|  | |

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

<a id="getFriendPermission"></a>
# **getFriendPermission**
> FriendPermissionGetResponse getFriendPermission(friendPermissionGetRequest)

Get friend permission

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.FriendshipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    FriendshipApi apiInstance = new FriendshipApi(defaultClient);
    
    FriendPermissionGetRequest friendPermissionGetRequest = new FriendPermissionGetRequest(); // FriendPermissionGetRequest | 
    try {
      FriendPermissionGetResponse result = apiInstance.getFriendPermission(friendPermissionGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FriendshipApi#getFriendPermission");
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
| **friendPermissionGetRequest** | [**FriendPermissionGetRequest**](FriendPermissionGetRequest.md)|  | |

### Return type

[**FriendPermissionGetResponse**](FriendPermissionGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getFriendRelationships"></a>
# **getFriendRelationships**
> FriendRelationshipGetResponse getFriendRelationships(friendRelationshipGetRequest)

Get friend relationships

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.FriendshipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    FriendshipApi apiInstance = new FriendshipApi(defaultClient);
    
    FriendRelationshipGetRequest friendRelationshipGetRequest = new FriendRelationshipGetRequest(); // FriendRelationshipGetRequest | 
    try {
      FriendRelationshipGetResponse result = apiInstance.getFriendRelationships(friendRelationshipGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FriendshipApi#getFriendRelationships");
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
| **friendRelationshipGetRequest** | [**FriendRelationshipGetRequest**](FriendRelationshipGetRequest.md)|  | |

### Return type

[**FriendRelationshipGetResponse**](FriendRelationshipGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listFriends"></a>
# **listFriends**
> FriendListResponse listFriends(friendListRequest)

List friends

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.FriendshipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    FriendshipApi apiInstance = new FriendshipApi(defaultClient);
    
    FriendListRequest friendListRequest = new FriendListRequest(); // FriendListRequest | 
    try {
      FriendListResponse result = apiInstance.listFriends(friendListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FriendshipApi#listFriends");
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
| **friendListRequest** | [**FriendListRequest**](FriendListRequest.md)|  | |

### Return type

[**FriendListResponse**](FriendListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="removeAllFriends"></a>
# **removeAllFriends**
> CodeOnlyResponse removeAllFriends(friendCleanRequest)

Clean all friends

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.FriendshipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    FriendshipApi apiInstance = new FriendshipApi(defaultClient);
    
    FriendCleanRequest friendCleanRequest = new FriendCleanRequest(); // FriendCleanRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeAllFriends(friendCleanRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FriendshipApi#removeAllFriends");
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
| **friendCleanRequest** | [**FriendCleanRequest**](FriendCleanRequest.md)|  | |

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

<a id="removeFriends"></a>
# **removeFriends**
> CodeOnlyResponse removeFriends(friendDeleteRequest)

Delete friends

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.FriendshipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    FriendshipApi apiInstance = new FriendshipApi(defaultClient);
    
    FriendDeleteRequest friendDeleteRequest = new FriendDeleteRequest(); // FriendDeleteRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeFriends(friendDeleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FriendshipApi#removeFriends");
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
| **friendDeleteRequest** | [**FriendDeleteRequest**](FriendDeleteRequest.md)|  | |

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

<a id="setFriendPermission"></a>
# **setFriendPermission**
> CodeOnlyResponse setFriendPermission(friendPermissionSetRequest)

Set friend permission

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.FriendshipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    FriendshipApi apiInstance = new FriendshipApi(defaultClient);
    
    FriendPermissionSetRequest friendPermissionSetRequest = new FriendPermissionSetRequest(); // FriendPermissionSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setFriendPermission(friendPermissionSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FriendshipApi#setFriendPermission");
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
| **friendPermissionSetRequest** | [**FriendPermissionSetRequest**](FriendPermissionSetRequest.md)|  | |

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

<a id="setFriendProfile"></a>
# **setFriendProfile**
> CodeOnlyResponse setFriendProfile(friendProfileSetRequest)

Set friend profile

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.FriendshipApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    FriendshipApi apiInstance = new FriendshipApi(defaultClient);
    
    FriendProfileSetRequest friendProfileSetRequest = new FriendProfileSetRequest(); // FriendProfileSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setFriendProfile(friendProfileSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FriendshipApi#setFriendProfile");
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
| **friendProfileSetRequest** | [**FriendProfileSetRequest**](FriendProfileSetRequest.md)|  | |

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

