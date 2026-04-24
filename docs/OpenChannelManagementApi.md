# OpenChannelManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createOpenChannel**](OpenChannelManagementApi.md#createOpenChannel) | **POST** /v4/open-channel/create | Create an open channel |
| [**destroyOpenChannels**](OpenChannelManagementApi.md#destroyOpenChannels) | **POST** /v4/open-channel/destroy | Destroy an open channel |
| [**getOpenChannel**](OpenChannelManagementApi.md#getOpenChannel) | **POST** /v4/open-channel/get | Get open channel info |
| [**setOpenChannelDestroyType**](OpenChannelManagementApi.md#setOpenChannelDestroyType) | **POST** /v4/open-channel/destroy-type/set | Set auto-destroy type |


<a id="createOpenChannel"></a>
# **createOpenChannel**
> CodeOnlyResponse createOpenChannel(openChannelCreateRequest)

Create an open channel

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelManagementApi apiInstance = new OpenChannelManagementApi(defaultClient);
    
    OpenChannelCreateRequest openChannelCreateRequest = new OpenChannelCreateRequest(); // OpenChannelCreateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.createOpenChannel(openChannelCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelManagementApi#createOpenChannel");
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
| **openChannelCreateRequest** | [**OpenChannelCreateRequest**](OpenChannelCreateRequest.md)|  | |

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

<a id="destroyOpenChannels"></a>
# **destroyOpenChannels**
> CodeOnlyResponse destroyOpenChannels(openChannelDestroyRequest)

Destroy an open channel

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelManagementApi apiInstance = new OpenChannelManagementApi(defaultClient);
    
    OpenChannelDestroyRequest openChannelDestroyRequest = new OpenChannelDestroyRequest(); // OpenChannelDestroyRequest | 
    try {
      CodeOnlyResponse result = apiInstance.destroyOpenChannels(openChannelDestroyRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelManagementApi#destroyOpenChannels");
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
| **openChannelDestroyRequest** | [**OpenChannelDestroyRequest**](OpenChannelDestroyRequest.md)|  | |

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

<a id="getOpenChannel"></a>
# **getOpenChannel**
> OpenChannelGetResponse getOpenChannel(openChannelGetRequest)

Get open channel info

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelManagementApi apiInstance = new OpenChannelManagementApi(defaultClient);
    
    OpenChannelGetRequest openChannelGetRequest = new OpenChannelGetRequest(); // OpenChannelGetRequest | 
    try {
      OpenChannelGetResponse result = apiInstance.getOpenChannel(openChannelGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelManagementApi#getOpenChannel");
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
| **openChannelGetRequest** | [**OpenChannelGetRequest**](OpenChannelGetRequest.md)|  | |

### Return type

[**OpenChannelGetResponse**](OpenChannelGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="setOpenChannelDestroyType"></a>
# **setOpenChannelDestroyType**
> CodeOnlyResponse setOpenChannelDestroyType(openChannelDestroyTypeSetRequest)

Set auto-destroy type

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelManagementApi apiInstance = new OpenChannelManagementApi(defaultClient);
    
    OpenChannelDestroyTypeSetRequest openChannelDestroyTypeSetRequest = new OpenChannelDestroyTypeSetRequest(); // OpenChannelDestroyTypeSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setOpenChannelDestroyType(openChannelDestroyTypeSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelManagementApi#setOpenChannelDestroyType");
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
| **openChannelDestroyTypeSetRequest** | [**OpenChannelDestroyTypeSetRequest**](OpenChannelDestroyTypeSetRequest.md)|  | |

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

