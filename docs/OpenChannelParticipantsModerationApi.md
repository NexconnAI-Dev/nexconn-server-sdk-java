# OpenChannelParticipantsModerationApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addOpenChannelFreezeList**](OpenChannelParticipantsModerationApi.md#addOpenChannelFreezeList) | **POST** /v4/open-channel/freeze-list/add | Freeze an open channel |
| [**addOpenChannelGlobalMuteList**](OpenChannelParticipantsModerationApi.md#addOpenChannelGlobalMuteList) | **POST** /v4/open-channel/global-mute-list/add | Mute a user globally |
| [**addOpenChannelParticipantAllowedSenderList**](OpenChannelParticipantsModerationApi.md#addOpenChannelParticipantAllowedSenderList) | **POST** /v4/open-channel/participant/allowed-sender-list/add | Add to allowed senders list |
| [**addOpenChannelParticipantBanList**](OpenChannelParticipantsModerationApi.md#addOpenChannelParticipantBanList) | **POST** /v4/open-channel/participant/ban-list/add | Ban a participant |
| [**addOpenChannelParticipantMuteList**](OpenChannelParticipantsModerationApi.md#addOpenChannelParticipantMuteList) | **POST** /v4/open-channel/participant/mute-list/add | Mute a participant |
| [**checkOpenChannelFreeze**](OpenChannelParticipantsModerationApi.md#checkOpenChannelFreeze) | **POST** /v4/open-channel/freeze/check | Check open channel freeze status |
| [**checkOpenChannelParticipantsExist**](OpenChannelParticipantsModerationApi.md#checkOpenChannelParticipantsExist) | **POST** /v4/open-channel/participant/exist | Batch check participants |
| [**getOpenChannelGlobalMuteList**](OpenChannelParticipantsModerationApi.md#getOpenChannelGlobalMuteList) | **POST** /v4/open-channel/global-mute-list/get | List globally muted users |
| [**getOpenChannelParticipantAllowedSenderList**](OpenChannelParticipantsModerationApi.md#getOpenChannelParticipantAllowedSenderList) | **POST** /v4/open-channel/participant/allowed-sender-list/get | Query allowed senders list |
| [**getOpenChannelParticipantBanList**](OpenChannelParticipantsModerationApi.md#getOpenChannelParticipantBanList) | **POST** /v4/open-channel/participant/ban-list/get | List banned participants |
| [**getOpenChannelParticipantMuteList**](OpenChannelParticipantsModerationApi.md#getOpenChannelParticipantMuteList) | **POST** /v4/open-channel/participant/mute-list/get | List muted participants |
| [**listFrozenOpenChannels**](OpenChannelParticipantsModerationApi.md#listFrozenOpenChannels) | **POST** /v4/open-channel/freeze-list/get | List frozen open channels |
| [**listOpenChannelParticipants**](OpenChannelParticipantsModerationApi.md#listOpenChannelParticipants) | **POST** /v4/open-channel/participant/list | List participants |
| [**removeOpenChannelFreezeList**](OpenChannelParticipantsModerationApi.md#removeOpenChannelFreezeList) | **POST** /v4/open-channel/freeze-list/remove | Unfreeze an open channel |
| [**removeOpenChannelGlobalMuteList**](OpenChannelParticipantsModerationApi.md#removeOpenChannelGlobalMuteList) | **POST** /v4/open-channel/global-mute-list/remove | Unmute a user globally |
| [**removeOpenChannelParticipantAllowedSenderList**](OpenChannelParticipantsModerationApi.md#removeOpenChannelParticipantAllowedSenderList) | **POST** /v4/open-channel/participant/allowed-sender-list/remove | Remove from allowed senders list |
| [**removeOpenChannelParticipantBanList**](OpenChannelParticipantsModerationApi.md#removeOpenChannelParticipantBanList) | **POST** /v4/open-channel/participant/ban-list/remove | Unban a participant |
| [**removeOpenChannelParticipantMuteList**](OpenChannelParticipantsModerationApi.md#removeOpenChannelParticipantMuteList) | **POST** /v4/open-channel/participant/mute-list/remove | Unmute a participant |


<a id="addOpenChannelFreezeList"></a>
# **addOpenChannelFreezeList**
> CodeOnlyResponse addOpenChannelFreezeList(openChannelFreezeListUpdateRequest)

Freeze an open channel

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelFreezeListUpdateRequest openChannelFreezeListUpdateRequest = new OpenChannelFreezeListUpdateRequest(); // OpenChannelFreezeListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addOpenChannelFreezeList(openChannelFreezeListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#addOpenChannelFreezeList");
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
| **openChannelFreezeListUpdateRequest** | [**OpenChannelFreezeListUpdateRequest**](OpenChannelFreezeListUpdateRequest.md)|  | |

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

<a id="addOpenChannelGlobalMuteList"></a>
# **addOpenChannelGlobalMuteList**
> CodeOnlyResponse addOpenChannelGlobalMuteList(openChannelGlobalMuteListAddRequest)

Mute a user globally

Rate limit: 100/sec. The public endpoint list currently publishes this capability as &#x60;/v4/open-channel/participant/global-mute-list/add&#x60;.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelGlobalMuteListAddRequest openChannelGlobalMuteListAddRequest = new OpenChannelGlobalMuteListAddRequest(); // OpenChannelGlobalMuteListAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addOpenChannelGlobalMuteList(openChannelGlobalMuteListAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#addOpenChannelGlobalMuteList");
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
| **openChannelGlobalMuteListAddRequest** | [**OpenChannelGlobalMuteListAddRequest**](OpenChannelGlobalMuteListAddRequest.md)|  | |

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

<a id="addOpenChannelParticipantAllowedSenderList"></a>
# **addOpenChannelParticipantAllowedSenderList**
> CodeOnlyResponse addOpenChannelParticipantAllowedSenderList(openChannelAllowedSenderListUpdateRequest)

Add to allowed senders list

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelAllowedSenderListUpdateRequest openChannelAllowedSenderListUpdateRequest = new OpenChannelAllowedSenderListUpdateRequest(); // OpenChannelAllowedSenderListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addOpenChannelParticipantAllowedSenderList(openChannelAllowedSenderListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#addOpenChannelParticipantAllowedSenderList");
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
| **openChannelAllowedSenderListUpdateRequest** | [**OpenChannelAllowedSenderListUpdateRequest**](OpenChannelAllowedSenderListUpdateRequest.md)|  | |

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

<a id="addOpenChannelParticipantBanList"></a>
# **addOpenChannelParticipantBanList**
> CodeOnlyResponse addOpenChannelParticipantBanList(openChannelParticipantMuteListAddRequest)

Ban a participant

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelParticipantMuteListAddRequest openChannelParticipantMuteListAddRequest = new OpenChannelParticipantMuteListAddRequest(); // OpenChannelParticipantMuteListAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addOpenChannelParticipantBanList(openChannelParticipantMuteListAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#addOpenChannelParticipantBanList");
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
| **openChannelParticipantMuteListAddRequest** | [**OpenChannelParticipantMuteListAddRequest**](OpenChannelParticipantMuteListAddRequest.md)|  | |

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

<a id="addOpenChannelParticipantMuteList"></a>
# **addOpenChannelParticipantMuteList**
> CodeOnlyResponse addOpenChannelParticipantMuteList(openChannelParticipantMuteListAddRequest)

Mute a participant

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelParticipantMuteListAddRequest openChannelParticipantMuteListAddRequest = new OpenChannelParticipantMuteListAddRequest(); // OpenChannelParticipantMuteListAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addOpenChannelParticipantMuteList(openChannelParticipantMuteListAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#addOpenChannelParticipantMuteList");
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
| **openChannelParticipantMuteListAddRequest** | [**OpenChannelParticipantMuteListAddRequest**](OpenChannelParticipantMuteListAddRequest.md)|  | |

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

<a id="checkOpenChannelFreeze"></a>
# **checkOpenChannelFreeze**
> OpenChannelFreezeCheckResponse checkOpenChannelFreeze(openChannelFreezeCheckRequest)

Check open channel freeze status

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelFreezeCheckRequest openChannelFreezeCheckRequest = new OpenChannelFreezeCheckRequest(); // OpenChannelFreezeCheckRequest | 
    try {
      OpenChannelFreezeCheckResponse result = apiInstance.checkOpenChannelFreeze(openChannelFreezeCheckRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#checkOpenChannelFreeze");
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
| **openChannelFreezeCheckRequest** | [**OpenChannelFreezeCheckRequest**](OpenChannelFreezeCheckRequest.md)|  | |

### Return type

[**OpenChannelFreezeCheckResponse**](OpenChannelFreezeCheckResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="checkOpenChannelParticipantsExist"></a>
# **checkOpenChannelParticipantsExist**
> OpenChannelParticipantExistResponse checkOpenChannelParticipantsExist(openChannelParticipantExistRequest)

Batch check participants

Rate limit: 100/sec. The same endpoint is also documented for single-user participant checks.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelParticipantExistRequest openChannelParticipantExistRequest = new OpenChannelParticipantExistRequest(); // OpenChannelParticipantExistRequest | 
    try {
      OpenChannelParticipantExistResponse result = apiInstance.checkOpenChannelParticipantsExist(openChannelParticipantExistRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#checkOpenChannelParticipantsExist");
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
| **openChannelParticipantExistRequest** | [**OpenChannelParticipantExistRequest**](OpenChannelParticipantExistRequest.md)|  | |

### Return type

[**OpenChannelParticipantExistResponse**](OpenChannelParticipantExistResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getOpenChannelGlobalMuteList"></a>
# **getOpenChannelGlobalMuteList**
> OpenChannelParticipantMuteListGetResponse getOpenChannelGlobalMuteList()

List globally muted users

Rate limit: 100/sec. The public endpoint list currently publishes this capability as &#x60;/v4/open-channel/participant/global-mute-list/get&#x60;.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    try {
      OpenChannelParticipantMuteListGetResponse result = apiInstance.getOpenChannelGlobalMuteList();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#getOpenChannelGlobalMuteList");
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

[**OpenChannelParticipantMuteListGetResponse**](OpenChannelParticipantMuteListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getOpenChannelParticipantAllowedSenderList"></a>
# **getOpenChannelParticipantAllowedSenderList**
> OpenChannelAllowedSenderListGetResponse getOpenChannelParticipantAllowedSenderList(openChannelParticipantListByChannelRequest)

Query allowed senders list

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelParticipantListByChannelRequest openChannelParticipantListByChannelRequest = new OpenChannelParticipantListByChannelRequest(); // OpenChannelParticipantListByChannelRequest | 
    try {
      OpenChannelAllowedSenderListGetResponse result = apiInstance.getOpenChannelParticipantAllowedSenderList(openChannelParticipantListByChannelRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#getOpenChannelParticipantAllowedSenderList");
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

[**OpenChannelAllowedSenderListGetResponse**](OpenChannelAllowedSenderListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getOpenChannelParticipantBanList"></a>
# **getOpenChannelParticipantBanList**
> OpenChannelParticipantBanListGetResponse getOpenChannelParticipantBanList(openChannelParticipantListByChannelRequest)

List banned participants

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelParticipantListByChannelRequest openChannelParticipantListByChannelRequest = new OpenChannelParticipantListByChannelRequest(); // OpenChannelParticipantListByChannelRequest | 
    try {
      OpenChannelParticipantBanListGetResponse result = apiInstance.getOpenChannelParticipantBanList(openChannelParticipantListByChannelRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#getOpenChannelParticipantBanList");
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

[**OpenChannelParticipantBanListGetResponse**](OpenChannelParticipantBanListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getOpenChannelParticipantMuteList"></a>
# **getOpenChannelParticipantMuteList**
> OpenChannelParticipantMuteListGetResponse getOpenChannelParticipantMuteList(openChannelParticipantListByChannelRequest)

List muted participants

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelParticipantListByChannelRequest openChannelParticipantListByChannelRequest = new OpenChannelParticipantListByChannelRequest(); // OpenChannelParticipantListByChannelRequest | 
    try {
      OpenChannelParticipantMuteListGetResponse result = apiInstance.getOpenChannelParticipantMuteList(openChannelParticipantListByChannelRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#getOpenChannelParticipantMuteList");
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

[**OpenChannelParticipantMuteListGetResponse**](OpenChannelParticipantMuteListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listFrozenOpenChannels"></a>
# **listFrozenOpenChannels**
> OpenChannelFreezeListGetResponse listFrozenOpenChannels(openChannelFreezeListGetRequest)

List frozen open channels

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelFreezeListGetRequest openChannelFreezeListGetRequest = new OpenChannelFreezeListGetRequest(); // OpenChannelFreezeListGetRequest | 
    try {
      OpenChannelFreezeListGetResponse result = apiInstance.listFrozenOpenChannels(openChannelFreezeListGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#listFrozenOpenChannels");
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
| **openChannelFreezeListGetRequest** | [**OpenChannelFreezeListGetRequest**](OpenChannelFreezeListGetRequest.md)|  | |

### Return type

[**OpenChannelFreezeListGetResponse**](OpenChannelFreezeListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listOpenChannelParticipants"></a>
# **listOpenChannelParticipants**
> OpenChannelParticipantListResponse listOpenChannelParticipants(openChannelParticipantListRequest)

List participants

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelParticipantListRequest openChannelParticipantListRequest = new OpenChannelParticipantListRequest(); // OpenChannelParticipantListRequest | 
    try {
      OpenChannelParticipantListResponse result = apiInstance.listOpenChannelParticipants(openChannelParticipantListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#listOpenChannelParticipants");
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
| **openChannelParticipantListRequest** | [**OpenChannelParticipantListRequest**](OpenChannelParticipantListRequest.md)|  | |

### Return type

[**OpenChannelParticipantListResponse**](OpenChannelParticipantListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="removeOpenChannelFreezeList"></a>
# **removeOpenChannelFreezeList**
> CodeOnlyResponse removeOpenChannelFreezeList(openChannelFreezeListUpdateRequest)

Unfreeze an open channel

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelFreezeListUpdateRequest openChannelFreezeListUpdateRequest = new OpenChannelFreezeListUpdateRequest(); // OpenChannelFreezeListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeOpenChannelFreezeList(openChannelFreezeListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#removeOpenChannelFreezeList");
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
| **openChannelFreezeListUpdateRequest** | [**OpenChannelFreezeListUpdateRequest**](OpenChannelFreezeListUpdateRequest.md)|  | |

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

<a id="removeOpenChannelGlobalMuteList"></a>
# **removeOpenChannelGlobalMuteList**
> CodeOnlyResponse removeOpenChannelGlobalMuteList(openChannelGlobalMuteListRemoveRequest)

Unmute a user globally

Rate limit: 100/sec. The public endpoint list currently publishes this capability as &#x60;/v4/open-channel/participant/global-mute-list/remove&#x60;.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelGlobalMuteListRemoveRequest openChannelGlobalMuteListRemoveRequest = new OpenChannelGlobalMuteListRemoveRequest(); // OpenChannelGlobalMuteListRemoveRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeOpenChannelGlobalMuteList(openChannelGlobalMuteListRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#removeOpenChannelGlobalMuteList");
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
| **openChannelGlobalMuteListRemoveRequest** | [**OpenChannelGlobalMuteListRemoveRequest**](OpenChannelGlobalMuteListRemoveRequest.md)|  | |

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

<a id="removeOpenChannelParticipantAllowedSenderList"></a>
# **removeOpenChannelParticipantAllowedSenderList**
> CodeOnlyResponse removeOpenChannelParticipantAllowedSenderList(openChannelAllowedSenderListUpdateRequest)

Remove from allowed senders list

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelAllowedSenderListUpdateRequest openChannelAllowedSenderListUpdateRequest = new OpenChannelAllowedSenderListUpdateRequest(); // OpenChannelAllowedSenderListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeOpenChannelParticipantAllowedSenderList(openChannelAllowedSenderListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#removeOpenChannelParticipantAllowedSenderList");
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
| **openChannelAllowedSenderListUpdateRequest** | [**OpenChannelAllowedSenderListUpdateRequest**](OpenChannelAllowedSenderListUpdateRequest.md)|  | |

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

<a id="removeOpenChannelParticipantBanList"></a>
# **removeOpenChannelParticipantBanList**
> CodeOnlyResponse removeOpenChannelParticipantBanList(openChannelParticipantMuteListRemoveRequest)

Unban a participant

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelParticipantMuteListRemoveRequest openChannelParticipantMuteListRemoveRequest = new OpenChannelParticipantMuteListRemoveRequest(); // OpenChannelParticipantMuteListRemoveRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeOpenChannelParticipantBanList(openChannelParticipantMuteListRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#removeOpenChannelParticipantBanList");
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
| **openChannelParticipantMuteListRemoveRequest** | [**OpenChannelParticipantMuteListRemoveRequest**](OpenChannelParticipantMuteListRemoveRequest.md)|  | |

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

<a id="removeOpenChannelParticipantMuteList"></a>
# **removeOpenChannelParticipantMuteList**
> CodeOnlyResponse removeOpenChannelParticipantMuteList(openChannelParticipantMuteListRemoveRequest)

Unmute a participant

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.OpenChannelParticipantsModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    OpenChannelParticipantsModerationApi apiInstance = new OpenChannelParticipantsModerationApi(defaultClient);
    
    OpenChannelParticipantMuteListRemoveRequest openChannelParticipantMuteListRemoveRequest = new OpenChannelParticipantMuteListRemoveRequest(); // OpenChannelParticipantMuteListRemoveRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeOpenChannelParticipantMuteList(openChannelParticipantMuteListRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OpenChannelParticipantsModerationApi#removeOpenChannelParticipantMuteList");
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
| **openChannelParticipantMuteListRemoveRequest** | [**OpenChannelParticipantMuteListRemoveRequest**](OpenChannelParticipantMuteListRemoveRequest.md)|  | |

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

