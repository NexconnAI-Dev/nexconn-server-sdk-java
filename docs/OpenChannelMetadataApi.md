# OpenChannelMetadataApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**batchGetOpenChannelMetadata**](OpenChannelMetadataApi.md#batchGetOpenChannelMetadata) | **POST** /v4/open-channel/metadata/batch/get | Query metadata |
| [**batchRemoveOpenChannelMetadata**](OpenChannelMetadataApi.md#batchRemoveOpenChannelMetadata) | **POST** /v4/open-channel/metadata/batch/remove | Batch delete metadata |
| [**batchSetOpenChannelMetadata**](OpenChannelMetadataApi.md#batchSetOpenChannelMetadata) | **POST** /v4/open-channel/metadata/batch/set | Batch set metadata |


<a id="batchGetOpenChannelMetadata"></a>
# **batchGetOpenChannelMetadata**
> OpenChannelMetadataBatchGetResponse batchGetOpenChannelMetadata(openChannelMetadataBatchGetRequest)

Query metadata

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelMetadataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelMetadataApi apiInstance = new OpenChannelMetadataApi(defaultClient);
    
    OpenChannelMetadataBatchGetRequest openChannelMetadataBatchGetRequest = new OpenChannelMetadataBatchGetRequest(); // OpenChannelMetadataBatchGetRequest | 
    try {
      OpenChannelMetadataBatchGetResponse result = apiInstance.batchGetOpenChannelMetadata(openChannelMetadataBatchGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelMetadataApi#batchGetOpenChannelMetadata");
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
| **openChannelMetadataBatchGetRequest** | [**OpenChannelMetadataBatchGetRequest**](OpenChannelMetadataBatchGetRequest.md)|  | |

### Return type

[**OpenChannelMetadataBatchGetResponse**](OpenChannelMetadataBatchGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="batchRemoveOpenChannelMetadata"></a>
# **batchRemoveOpenChannelMetadata**
> CodeOnlyResponse batchRemoveOpenChannelMetadata(openChannelMetadataBatchRemoveRequest)

Batch delete metadata

Rate limit: 100 attrs/sec (shared).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelMetadataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelMetadataApi apiInstance = new OpenChannelMetadataApi(defaultClient);
    
    OpenChannelMetadataBatchRemoveRequest openChannelMetadataBatchRemoveRequest = new OpenChannelMetadataBatchRemoveRequest(); // OpenChannelMetadataBatchRemoveRequest | 
    try {
      CodeOnlyResponse result = apiInstance.batchRemoveOpenChannelMetadata(openChannelMetadataBatchRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelMetadataApi#batchRemoveOpenChannelMetadata");
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
| **openChannelMetadataBatchRemoveRequest** | [**OpenChannelMetadataBatchRemoveRequest**](OpenChannelMetadataBatchRemoveRequest.md)|  | |

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

<a id="batchSetOpenChannelMetadata"></a>
# **batchSetOpenChannelMetadata**
> CodeOnlyResponse batchSetOpenChannelMetadata(openChannelMetadataBatchSetRequest)

Batch set metadata

Rate limit: 100 attrs/sec (shared).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelMetadataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelMetadataApi apiInstance = new OpenChannelMetadataApi(defaultClient);
    
    OpenChannelMetadataBatchSetRequest openChannelMetadataBatchSetRequest = new OpenChannelMetadataBatchSetRequest(); // OpenChannelMetadataBatchSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.batchSetOpenChannelMetadata(openChannelMetadataBatchSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelMetadataApi#batchSetOpenChannelMetadata");
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
| **openChannelMetadataBatchSetRequest** | [**OpenChannelMetadataBatchSetRequest**](OpenChannelMetadataBatchSetRequest.md)|  | |

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

