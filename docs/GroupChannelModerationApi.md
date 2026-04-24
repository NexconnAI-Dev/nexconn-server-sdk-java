# GroupChannelModerationApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addGroupChannelAllowedSenderList**](GroupChannelModerationApi.md#addGroupChannelAllowedSenderList) | **POST** /v4/group-channel/allowed-sender-list/add | Add to allowed senders list |
| [**addGroupChannelFreezeList**](GroupChannelModerationApi.md#addGroupChannelFreezeList) | **POST** /v4/group-channel/freeze-list/add | Freeze a group |
| [**addGroupChannelUserMuteList**](GroupChannelModerationApi.md#addGroupChannelUserMuteList) | **POST** /v4/group-channel/user/mute-list/add | Mute a group member |
| [**getGroupChannelAllowedSenderList**](GroupChannelModerationApi.md#getGroupChannelAllowedSenderList) | **POST** /v4/group-channel/allowed-sender-list/get | Query allowed senders list |
| [**getGroupChannelFreezeList**](GroupChannelModerationApi.md#getGroupChannelFreezeList) | **POST** /v4/group-channel/freeze-list/get | Query group freeze status |
| [**getGroupChannelUserMuteList**](GroupChannelModerationApi.md#getGroupChannelUserMuteList) | **POST** /v4/group-channel/user/mute-list/get | List muted group members |
| [**removeGroupChannelAllowedSenderList**](GroupChannelModerationApi.md#removeGroupChannelAllowedSenderList) | **POST** /v4/group-channel/allowed-sender-list/remove | Remove from allowed senders list |
| [**removeGroupChannelFreezeList**](GroupChannelModerationApi.md#removeGroupChannelFreezeList) | **POST** /v4/group-channel/freeze-list/remove | Unfreeze a group |
| [**removeGroupChannelUserMuteList**](GroupChannelModerationApi.md#removeGroupChannelUserMuteList) | **POST** /v4/group-channel/user/mute-list/remove | Unmute a group member |


<a id="addGroupChannelAllowedSenderList"></a>
# **addGroupChannelAllowedSenderList**
> CodeOnlyResponse addGroupChannelAllowedSenderList(groupChannelAllowedSenderListUpdateRequest)

Add to allowed senders list

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelModerationApi apiInstance = new GroupChannelModerationApi(defaultClient);
    
    GroupChannelAllowedSenderListUpdateRequest groupChannelAllowedSenderListUpdateRequest = new GroupChannelAllowedSenderListUpdateRequest(); // GroupChannelAllowedSenderListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addGroupChannelAllowedSenderList(groupChannelAllowedSenderListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelModerationApi#addGroupChannelAllowedSenderList");
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
| **groupChannelAllowedSenderListUpdateRequest** | [**GroupChannelAllowedSenderListUpdateRequest**](GroupChannelAllowedSenderListUpdateRequest.md)|  | |

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

<a id="addGroupChannelFreezeList"></a>
# **addGroupChannelFreezeList**
> CodeOnlyResponse addGroupChannelFreezeList(groupChannelFreezeListUpdateRequest)

Freeze a group

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelModerationApi apiInstance = new GroupChannelModerationApi(defaultClient);
    
    GroupChannelFreezeListUpdateRequest groupChannelFreezeListUpdateRequest = new GroupChannelFreezeListUpdateRequest(); // GroupChannelFreezeListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addGroupChannelFreezeList(groupChannelFreezeListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelModerationApi#addGroupChannelFreezeList");
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
| **groupChannelFreezeListUpdateRequest** | [**GroupChannelFreezeListUpdateRequest**](GroupChannelFreezeListUpdateRequest.md)|  | |

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

<a id="addGroupChannelUserMuteList"></a>
# **addGroupChannelUserMuteList**
> CodeOnlyResponse addGroupChannelUserMuteList(groupChannelUserMuteListAddRequest)

Mute a group member

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelModerationApi apiInstance = new GroupChannelModerationApi(defaultClient);
    
    GroupChannelUserMuteListAddRequest groupChannelUserMuteListAddRequest = new GroupChannelUserMuteListAddRequest(); // GroupChannelUserMuteListAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addGroupChannelUserMuteList(groupChannelUserMuteListAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelModerationApi#addGroupChannelUserMuteList");
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
| **groupChannelUserMuteListAddRequest** | [**GroupChannelUserMuteListAddRequest**](GroupChannelUserMuteListAddRequest.md)|  | |

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

<a id="getGroupChannelAllowedSenderList"></a>
# **getGroupChannelAllowedSenderList**
> GroupChannelAllowedSenderListGetResponse getGroupChannelAllowedSenderList(groupChannelAllowedSenderListGetRequest)

Query allowed senders list

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelModerationApi apiInstance = new GroupChannelModerationApi(defaultClient);
    
    GroupChannelAllowedSenderListGetRequest groupChannelAllowedSenderListGetRequest = new GroupChannelAllowedSenderListGetRequest(); // GroupChannelAllowedSenderListGetRequest | 
    try {
      GroupChannelAllowedSenderListGetResponse result = apiInstance.getGroupChannelAllowedSenderList(groupChannelAllowedSenderListGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelModerationApi#getGroupChannelAllowedSenderList");
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
| **groupChannelAllowedSenderListGetRequest** | [**GroupChannelAllowedSenderListGetRequest**](GroupChannelAllowedSenderListGetRequest.md)|  | |

### Return type

[**GroupChannelAllowedSenderListGetResponse**](GroupChannelAllowedSenderListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getGroupChannelFreezeList"></a>
# **getGroupChannelFreezeList**
> GroupChannelFreezeListGetResponse getGroupChannelFreezeList(groupChannelFreezeListGetRequest)

Query group freeze status

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelModerationApi apiInstance = new GroupChannelModerationApi(defaultClient);
    
    GroupChannelFreezeListGetRequest groupChannelFreezeListGetRequest = new GroupChannelFreezeListGetRequest(); // GroupChannelFreezeListGetRequest | 
    try {
      GroupChannelFreezeListGetResponse result = apiInstance.getGroupChannelFreezeList(groupChannelFreezeListGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelModerationApi#getGroupChannelFreezeList");
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
| **groupChannelFreezeListGetRequest** | [**GroupChannelFreezeListGetRequest**](GroupChannelFreezeListGetRequest.md)|  | |

### Return type

[**GroupChannelFreezeListGetResponse**](GroupChannelFreezeListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getGroupChannelUserMuteList"></a>
# **getGroupChannelUserMuteList**
> GroupChannelUserMuteListGetResponse getGroupChannelUserMuteList(groupChannelUserMuteListGetRequest)

List muted group members

Rate limit: 100/sec. The public endpoint list currently publishes this capability as &#x60;/v4/group-channel/user/mute-list-get&#x60;.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelModerationApi apiInstance = new GroupChannelModerationApi(defaultClient);
    
    GroupChannelUserMuteListGetRequest groupChannelUserMuteListGetRequest = new GroupChannelUserMuteListGetRequest(); // GroupChannelUserMuteListGetRequest | 
    try {
      GroupChannelUserMuteListGetResponse result = apiInstance.getGroupChannelUserMuteList(groupChannelUserMuteListGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelModerationApi#getGroupChannelUserMuteList");
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
| **groupChannelUserMuteListGetRequest** | [**GroupChannelUserMuteListGetRequest**](GroupChannelUserMuteListGetRequest.md)|  | |

### Return type

[**GroupChannelUserMuteListGetResponse**](GroupChannelUserMuteListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="removeGroupChannelAllowedSenderList"></a>
# **removeGroupChannelAllowedSenderList**
> CodeOnlyResponse removeGroupChannelAllowedSenderList(groupChannelAllowedSenderListUpdateRequest)

Remove from allowed senders list

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelModerationApi apiInstance = new GroupChannelModerationApi(defaultClient);
    
    GroupChannelAllowedSenderListUpdateRequest groupChannelAllowedSenderListUpdateRequest = new GroupChannelAllowedSenderListUpdateRequest(); // GroupChannelAllowedSenderListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeGroupChannelAllowedSenderList(groupChannelAllowedSenderListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelModerationApi#removeGroupChannelAllowedSenderList");
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
| **groupChannelAllowedSenderListUpdateRequest** | [**GroupChannelAllowedSenderListUpdateRequest**](GroupChannelAllowedSenderListUpdateRequest.md)|  | |

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

<a id="removeGroupChannelFreezeList"></a>
# **removeGroupChannelFreezeList**
> CodeOnlyResponse removeGroupChannelFreezeList(groupChannelFreezeListUpdateRequest)

Unfreeze a group

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelModerationApi apiInstance = new GroupChannelModerationApi(defaultClient);
    
    GroupChannelFreezeListUpdateRequest groupChannelFreezeListUpdateRequest = new GroupChannelFreezeListUpdateRequest(); // GroupChannelFreezeListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeGroupChannelFreezeList(groupChannelFreezeListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelModerationApi#removeGroupChannelFreezeList");
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
| **groupChannelFreezeListUpdateRequest** | [**GroupChannelFreezeListUpdateRequest**](GroupChannelFreezeListUpdateRequest.md)|  | |

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

<a id="removeGroupChannelUserMuteList"></a>
# **removeGroupChannelUserMuteList**
> CodeOnlyResponse removeGroupChannelUserMuteList(groupChannelUserMuteListRemoveRequest)

Unmute a group member

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.GroupChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    GroupChannelModerationApi apiInstance = new GroupChannelModerationApi(defaultClient);
    
    GroupChannelUserMuteListRemoveRequest groupChannelUserMuteListRemoveRequest = new GroupChannelUserMuteListRemoveRequest(); // GroupChannelUserMuteListRemoveRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeGroupChannelUserMuteList(groupChannelUserMuteListRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GroupChannelModerationApi#removeGroupChannelUserMuteList");
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
| **groupChannelUserMuteListRemoveRequest** | [**GroupChannelUserMuteListRemoveRequest**](GroupChannelUserMuteListRemoveRequest.md)|  | |

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

