# OpenChannelMessagePriorityApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addOpenChannelLowPriorityMessageTypeList**](OpenChannelMessagePriorityApi.md#addOpenChannelLowPriorityMessageTypeList) | **POST** /v4/open-channel/low-priority-message-type-list/add | Add low-priority message types |
| [**getOpenChannelLowPriorityMessageTypeList**](OpenChannelMessagePriorityApi.md#getOpenChannelLowPriorityMessageTypeList) | **POST** /v4/open-channel/low-priority-message-type-list/get | Query low-priority message types |
| [**removeOpenChannelLowPriorityMessageTypeList**](OpenChannelMessagePriorityApi.md#removeOpenChannelLowPriorityMessageTypeList) | **POST** /v4/open-channel/low-priority-message-type-list/remove | Remove low-priority message types |


<a id="addOpenChannelLowPriorityMessageTypeList"></a>
# **addOpenChannelLowPriorityMessageTypeList**
> CodeOnlyResponse addOpenChannelLowPriorityMessageTypeList(openChannelLowPriorityMessageTypeListRequest)

Add low-priority message types

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelMessagePriorityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelMessagePriorityApi apiInstance = new OpenChannelMessagePriorityApi(defaultClient);
    
    OpenChannelLowPriorityMessageTypeListRequest openChannelLowPriorityMessageTypeListRequest = new OpenChannelLowPriorityMessageTypeListRequest(); // OpenChannelLowPriorityMessageTypeListRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addOpenChannelLowPriorityMessageTypeList(openChannelLowPriorityMessageTypeListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelMessagePriorityApi#addOpenChannelLowPriorityMessageTypeList");
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
| **openChannelLowPriorityMessageTypeListRequest** | [**OpenChannelLowPriorityMessageTypeListRequest**](OpenChannelLowPriorityMessageTypeListRequest.md)|  | |

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

<a id="getOpenChannelLowPriorityMessageTypeList"></a>
# **getOpenChannelLowPriorityMessageTypeList**
> OpenChannelMessageTypeListResponse getOpenChannelLowPriorityMessageTypeList()

Query low-priority message types

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelMessagePriorityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelMessagePriorityApi apiInstance = new OpenChannelMessagePriorityApi(defaultClient);
    try {
      OpenChannelMessageTypeListResponse result = apiInstance.getOpenChannelLowPriorityMessageTypeList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelMessagePriorityApi#getOpenChannelLowPriorityMessageTypeList");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not require a request body.

### Return type

[**OpenChannelMessageTypeListResponse**](OpenChannelMessageTypeListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="removeOpenChannelLowPriorityMessageTypeList"></a>
# **removeOpenChannelLowPriorityMessageTypeList**
> CodeOnlyResponse removeOpenChannelLowPriorityMessageTypeList(openChannelLowPriorityMessageTypeListRequest)

Remove low-priority message types

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelMessagePriorityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelMessagePriorityApi apiInstance = new OpenChannelMessagePriorityApi(defaultClient);
    
    OpenChannelLowPriorityMessageTypeListRequest openChannelLowPriorityMessageTypeListRequest = new OpenChannelLowPriorityMessageTypeListRequest(); // OpenChannelLowPriorityMessageTypeListRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeOpenChannelLowPriorityMessageTypeList(openChannelLowPriorityMessageTypeListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelMessagePriorityApi#removeOpenChannelLowPriorityMessageTypeList");
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
| **openChannelLowPriorityMessageTypeListRequest** | [**OpenChannelLowPriorityMessageTypeListRequest**](OpenChannelLowPriorityMessageTypeListRequest.md)|  | |

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

