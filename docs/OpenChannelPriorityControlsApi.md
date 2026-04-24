# OpenChannelPriorityControlsApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addOpenChannelPriorityMessageTypeList**](OpenChannelPriorityControlsApi.md#addOpenChannelPriorityMessageTypeList) | **POST** /v4/open-channel/priority-message-type-list/add | Add priority message types |
| [**addOpenChannelPrioritySenderList**](OpenChannelPriorityControlsApi.md#addOpenChannelPrioritySenderList) | **POST** /v4/open-channel/priority-sender-list/add | Add priority senders |
| [**getOpenChannelPriorityMessageTypeList**](OpenChannelPriorityControlsApi.md#getOpenChannelPriorityMessageTypeList) | **POST** /v4/open-channel/priority-message-type-list/get | Query priority message types |
| [**getOpenChannelPrioritySenderList**](OpenChannelPriorityControlsApi.md#getOpenChannelPrioritySenderList) | **POST** /v4/open-channel/priority-sender-list/get | Query priority senders |
| [**removeOpenChannelPriorityMessageTypeList**](OpenChannelPriorityControlsApi.md#removeOpenChannelPriorityMessageTypeList) | **POST** /v4/open-channel/priority-message-type-list/remove | Remove priority message types |
| [**removeOpenChannelPrioritySenderList**](OpenChannelPriorityControlsApi.md#removeOpenChannelPrioritySenderList) | **POST** /v4/open-channel/priority-sender-list/remove | Remove priority senders |


<a id="addOpenChannelPriorityMessageTypeList"></a>
# **addOpenChannelPriorityMessageTypeList**
> CodeOnlyResponse addOpenChannelPriorityMessageTypeList(openChannelPriorityMessageTypeListRequest)

Add priority message types

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelPriorityControlsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelPriorityControlsApi apiInstance = new OpenChannelPriorityControlsApi(defaultClient);
    
    OpenChannelPriorityMessageTypeListRequest openChannelPriorityMessageTypeListRequest = new OpenChannelPriorityMessageTypeListRequest(); // OpenChannelPriorityMessageTypeListRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addOpenChannelPriorityMessageTypeList(openChannelPriorityMessageTypeListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelPriorityControlsApi#addOpenChannelPriorityMessageTypeList");
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
| **openChannelPriorityMessageTypeListRequest** | [**OpenChannelPriorityMessageTypeListRequest**](OpenChannelPriorityMessageTypeListRequest.md)|  | |

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

<a id="addOpenChannelPrioritySenderList"></a>
# **addOpenChannelPrioritySenderList**
> CodeOnlyResponse addOpenChannelPrioritySenderList(openChannelParticipantIdsRequest)

Add priority senders

Rate limit: 100/sec. The public endpoint list currently publishes this capability as &#x60;/v4/open-channel/participant/priority-sender-list/add&#x60;.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelPriorityControlsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelPriorityControlsApi apiInstance = new OpenChannelPriorityControlsApi(defaultClient);
    
    OpenChannelParticipantIdsRequest openChannelParticipantIdsRequest = new OpenChannelParticipantIdsRequest(); // OpenChannelParticipantIdsRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addOpenChannelPrioritySenderList(openChannelParticipantIdsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelPriorityControlsApi#addOpenChannelPrioritySenderList");
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
| **openChannelParticipantIdsRequest** | [**OpenChannelParticipantIdsRequest**](OpenChannelParticipantIdsRequest.md)|  | |

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

<a id="getOpenChannelPriorityMessageTypeList"></a>
# **getOpenChannelPriorityMessageTypeList**
> OpenChannelMessageTypeListResponse getOpenChannelPriorityMessageTypeList()

Query priority message types

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelPriorityControlsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelPriorityControlsApi apiInstance = new OpenChannelPriorityControlsApi(defaultClient);
    try {
      OpenChannelMessageTypeListResponse result = apiInstance.getOpenChannelPriorityMessageTypeList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelPriorityControlsApi#getOpenChannelPriorityMessageTypeList");
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

<a id="getOpenChannelPrioritySenderList"></a>
# **getOpenChannelPrioritySenderList**
> OpenChannelParticipantIdsResponse getOpenChannelPrioritySenderList(openChannelParticipantListByChannelRequest)

Query priority senders

Rate limit: 100/sec. The public endpoint list currently publishes this capability as &#x60;/v4/open-channel/participant/priority-sender-list/get&#x60;.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelPriorityControlsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelPriorityControlsApi apiInstance = new OpenChannelPriorityControlsApi(defaultClient);
    
    OpenChannelParticipantListByChannelRequest openChannelParticipantListByChannelRequest = new OpenChannelParticipantListByChannelRequest(); // OpenChannelParticipantListByChannelRequest | 
    try {
      OpenChannelParticipantIdsResponse result = apiInstance.getOpenChannelPrioritySenderList(openChannelParticipantListByChannelRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelPriorityControlsApi#getOpenChannelPrioritySenderList");
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
| **openChannelParticipantListByChannelRequest** | [**OpenChannelParticipantListByChannelRequest**](OpenChannelParticipantListByChannelRequest.md)|  | |

### Return type

[**OpenChannelParticipantIdsResponse**](OpenChannelParticipantIdsResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="removeOpenChannelPriorityMessageTypeList"></a>
# **removeOpenChannelPriorityMessageTypeList**
> CodeOnlyResponse removeOpenChannelPriorityMessageTypeList(openChannelPriorityMessageTypeListRequest)

Remove priority message types

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelPriorityControlsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelPriorityControlsApi apiInstance = new OpenChannelPriorityControlsApi(defaultClient);
    
    OpenChannelPriorityMessageTypeListRequest openChannelPriorityMessageTypeListRequest = new OpenChannelPriorityMessageTypeListRequest(); // OpenChannelPriorityMessageTypeListRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeOpenChannelPriorityMessageTypeList(openChannelPriorityMessageTypeListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelPriorityControlsApi#removeOpenChannelPriorityMessageTypeList");
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
| **openChannelPriorityMessageTypeListRequest** | [**OpenChannelPriorityMessageTypeListRequest**](OpenChannelPriorityMessageTypeListRequest.md)|  | |

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

<a id="removeOpenChannelPrioritySenderList"></a>
# **removeOpenChannelPrioritySenderList**
> CodeOnlyResponse removeOpenChannelPrioritySenderList(openChannelParticipantIdsRequest)

Remove priority senders

Rate limit: 100/sec. The public endpoint list currently publishes this capability as &#x60;/v4/open-channel/participant/priority-sender-list/remove&#x60;.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelPriorityControlsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelPriorityControlsApi apiInstance = new OpenChannelPriorityControlsApi(defaultClient);
    
    OpenChannelParticipantIdsRequest openChannelParticipantIdsRequest = new OpenChannelParticipantIdsRequest(); // OpenChannelParticipantIdsRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeOpenChannelPrioritySenderList(openChannelParticipantIdsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelPriorityControlsApi#removeOpenChannelPrioritySenderList");
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
| **openChannelParticipantIdsRequest** | [**OpenChannelParticipantIdsRequest**](OpenChannelParticipantIdsRequest.md)|  | |

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

