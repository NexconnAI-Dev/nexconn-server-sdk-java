# ModerationApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**batchAddProfanityWords**](ModerationApi.md#batchAddProfanityWords) | **POST** /v4/profanity-word/batch/add | Batch add profanity words |
| [**batchRemoveProfanityWords**](ModerationApi.md#batchRemoveProfanityWords) | **POST** /v4/profanity-word/batch/remove | Batch delete profanity words |
| [**listProfanityWords**](ModerationApi.md#listProfanityWords) | **POST** /v4/profanity-word/list | List profanity words |
| [**removeProfanityWord**](ModerationApi.md#removeProfanityWord) | **POST** /v4/profanity-word/remove | Delete profanity word |


<a id="batchAddProfanityWords"></a>
# **batchAddProfanityWords**
> ProfanityWordBatchAddResponse batchAddProfanityWords(profanityWordBatchAddRequest)

Batch add profanity words

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ModerationApi apiInstance = new ModerationApi(defaultClient);
    
    ProfanityWordBatchAddRequest profanityWordBatchAddRequest = new ProfanityWordBatchAddRequest(); // ProfanityWordBatchAddRequest | 
    try {
      ProfanityWordBatchAddResponse result = apiInstance.batchAddProfanityWords(profanityWordBatchAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ModerationApi#batchAddProfanityWords");
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
| **profanityWordBatchAddRequest** | [**ProfanityWordBatchAddRequest**](ProfanityWordBatchAddRequest.md)|  | |

### Return type

[**ProfanityWordBatchAddResponse**](ProfanityWordBatchAddResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="batchRemoveProfanityWords"></a>
# **batchRemoveProfanityWords**
> CodeOnlyResponse batchRemoveProfanityWords(profanityWordBatchDeleteRequest)

Batch delete profanity words

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ModerationApi apiInstance = new ModerationApi(defaultClient);
    
    ProfanityWordBatchDeleteRequest profanityWordBatchDeleteRequest = new ProfanityWordBatchDeleteRequest(); // ProfanityWordBatchDeleteRequest | 
    try {
      CodeOnlyResponse result = apiInstance.batchRemoveProfanityWords(profanityWordBatchDeleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ModerationApi#batchRemoveProfanityWords");
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
| **profanityWordBatchDeleteRequest** | [**ProfanityWordBatchDeleteRequest**](ProfanityWordBatchDeleteRequest.md)|  | |

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

<a id="listProfanityWords"></a>
# **listProfanityWords**
> ProfanityWordListResponse listProfanityWords(profanityWordListRequest)

List profanity words

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ModerationApi apiInstance = new ModerationApi(defaultClient);
    
    ProfanityWordListRequest profanityWordListRequest = new ProfanityWordListRequest(); // ProfanityWordListRequest | 
    try {
      ProfanityWordListResponse result = apiInstance.listProfanityWords(profanityWordListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ModerationApi#listProfanityWords");
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
| **profanityWordListRequest** | [**ProfanityWordListRequest**](ProfanityWordListRequest.md)|  | |

### Return type

[**ProfanityWordListResponse**](ProfanityWordListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="removeProfanityWord"></a>
# **removeProfanityWord**
> CodeOnlyResponse removeProfanityWord(profanityWordDeleteRequest)

Delete profanity word

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ModerationApi apiInstance = new ModerationApi(defaultClient);
    
    ProfanityWordDeleteRequest profanityWordDeleteRequest = new ProfanityWordDeleteRequest(); // ProfanityWordDeleteRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeProfanityWord(profanityWordDeleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ModerationApi#removeProfanityWord");
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
| **profanityWordDeleteRequest** | [**ProfanityWordDeleteRequest**](ProfanityWordDeleteRequest.md)|  | |

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

