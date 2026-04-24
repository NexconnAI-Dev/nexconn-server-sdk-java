# UserProfileHostingApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**batchGetUserProfiles**](UserProfileHostingApi.md#batchGetUserProfiles) | **POST** /v4/user/profile/batch/get | Batch get user profiles |
| [**deleteUserProfiles**](UserProfileHostingApi.md#deleteUserProfiles) | **POST** /v4/user/profile/delete | Clear user profiles |
| [**listUserProfiles**](UserProfileHostingApi.md#listUserProfiles) | **POST** /v4/user/profile/list | List user profiles |
| [**setUserProfile**](UserProfileHostingApi.md#setUserProfile) | **POST** /v4/user/profile/set | Set user profile |


<a id="batchGetUserProfiles"></a>
# **batchGetUserProfiles**
> UserProfileBatchGetResponse batchGetUserProfiles(userIdsMax20Request)

Batch get user profiles

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserProfileHostingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserProfileHostingApi apiInstance = new UserProfileHostingApi(defaultClient);
    
    UserIdsMax20Request userIdsMax20Request = new UserIdsMax20Request(); // UserIdsMax20Request | 
    try {
      UserProfileBatchGetResponse result = apiInstance.batchGetUserProfiles(userIdsMax20Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserProfileHostingApi#batchGetUserProfiles");
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

[**UserProfileBatchGetResponse**](UserProfileBatchGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="deleteUserProfiles"></a>
# **deleteUserProfiles**
> CodeOnlyResponse deleteUserProfiles(userIdsMax20Request)

Clear user profiles

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserProfileHostingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserProfileHostingApi apiInstance = new UserProfileHostingApi(defaultClient);
    
    UserIdsMax20Request userIdsMax20Request = new UserIdsMax20Request(); // UserIdsMax20Request | 
    try {
      CodeOnlyResponse result = apiInstance.deleteUserProfiles(userIdsMax20Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserProfileHostingApi#deleteUserProfiles");
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

<a id="listUserProfiles"></a>
# **listUserProfiles**
> UserProfileListResponse listUserProfiles(userProfileListRequest)

List user profiles

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserProfileHostingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserProfileHostingApi apiInstance = new UserProfileHostingApi(defaultClient);
    
    UserProfileListRequest userProfileListRequest = new UserProfileListRequest(); // UserProfileListRequest | 
    try {
      UserProfileListResponse result = apiInstance.listUserProfiles(userProfileListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserProfileHostingApi#listUserProfiles");
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
| **userProfileListRequest** | [**UserProfileListRequest**](UserProfileListRequest.md)|  | |

### Return type

[**UserProfileListResponse**](UserProfileListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="setUserProfile"></a>
# **setUserProfile**
> UserProfileSetResponse setUserProfile(userProfileSetRequest)

Set user profile

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserProfileHostingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserProfileHostingApi apiInstance = new UserProfileHostingApi(defaultClient);
    
    UserProfileSetRequest userProfileSetRequest = new UserProfileSetRequest(); // UserProfileSetRequest | 
    try {
      UserProfileSetResponse result = apiInstance.setUserProfile(userProfileSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserProfileHostingApi#setUserProfile");
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
| **userProfileSetRequest** | [**UserProfileSetRequest**](UserProfileSetRequest.md)|  | |

### Return type

[**UserProfileSetResponse**](UserProfileSetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

