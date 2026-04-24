# UserBlocklistApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addUserBlocklist**](UserBlocklistApi.md#addUserBlocklist) | **POST** /v4/user/blocklist/add | Add to blocklist |
| [**getUserBlocklist**](UserBlocklistApi.md#getUserBlocklist) | **POST** /v4/user/blocklist/get | Get blocklist |
| [**removeUserBlocklist**](UserBlocklistApi.md#removeUserBlocklist) | **POST** /v4/user/blocklist/remove | Remove from blocklist |


<a id="addUserBlocklist"></a>
# **addUserBlocklist**
> CodeOnlyResponse addUserBlocklist(userBlocklistAddRequest)

Add to blocklist

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserBlocklistApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserBlocklistApi apiInstance = new UserBlocklistApi(defaultClient);
    
    UserBlocklistAddRequest userBlocklistAddRequest = new UserBlocklistAddRequest(); // UserBlocklistAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addUserBlocklist(userBlocklistAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserBlocklistApi#addUserBlocklist");
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
| **userBlocklistAddRequest** | [**UserBlocklistAddRequest**](UserBlocklistAddRequest.md)|  | |

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

<a id="getUserBlocklist"></a>
# **getUserBlocklist**
> UserBlocklistGetResponse getUserBlocklist(userBlocklistGetRequest)

Get blocklist

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserBlocklistApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserBlocklistApi apiInstance = new UserBlocklistApi(defaultClient);
    
    UserBlocklistGetRequest userBlocklistGetRequest = new UserBlocklistGetRequest(); // UserBlocklistGetRequest | 
    try {
      UserBlocklistGetResponse result = apiInstance.getUserBlocklist(userBlocklistGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserBlocklistApi#getUserBlocklist");
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
| **userBlocklistGetRequest** | [**UserBlocklistGetRequest**](UserBlocklistGetRequest.md)|  | |

### Return type

[**UserBlocklistGetResponse**](UserBlocklistGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="removeUserBlocklist"></a>
# **removeUserBlocklist**
> CodeOnlyResponse removeUserBlocklist(userBlocklistRemoveRequest)

Remove from blocklist

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.UserBlocklistApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    UserBlocklistApi apiInstance = new UserBlocklistApi(defaultClient);
    
    UserBlocklistRemoveRequest userBlocklistRemoveRequest = new UserBlocklistRemoveRequest(); // UserBlocklistRemoveRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeUserBlocklist(userBlocklistRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserBlocklistApi#removeUserBlocklist");
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
| **userBlocklistRemoveRequest** | [**UserBlocklistRemoveRequest**](UserBlocklistRemoveRequest.md)|  | |

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

