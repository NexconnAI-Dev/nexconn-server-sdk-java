# CommunityChannelModerationApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addCommunityChannelAllowedSenderList**](CommunityChannelModerationApi.md#addCommunityChannelAllowedSenderList) | **POST** /v4/community-channel/allowed-sender-list/add | Add community channel allowed sender list |
| [**addCommunityChannelMutedUsers**](CommunityChannelModerationApi.md#addCommunityChannelMutedUsers) | **POST** /v4/community-channel/mute-list/add | Add community-channel muted users |
| [**getCommunityChannelFreezeList**](CommunityChannelModerationApi.md#getCommunityChannelFreezeList) | **POST** /v4/community-channel/freeze-list/get | Get community channel freeze status |
| [**listCommunityChannelAllowedSenderList**](CommunityChannelModerationApi.md#listCommunityChannelAllowedSenderList) | **POST** /v4/community-channel/allowed-sender-list/get | List community channel allowed sender list |
| [**listCommunityChannelMutedUsers**](CommunityChannelModerationApi.md#listCommunityChannelMutedUsers) | **POST** /v4/community-channel/mute-list/get | List community-channel muted users |
| [**removeCommunityChannelAllowedSenderList**](CommunityChannelModerationApi.md#removeCommunityChannelAllowedSenderList) | **POST** /v4/community-channel/allowed-sender-list/remove | Remove community channel allowed sender list |
| [**removeCommunityChannelMutedUsers**](CommunityChannelModerationApi.md#removeCommunityChannelMutedUsers) | **POST** /v4/community-channel/mute-list/remove | Remove community-channel muted users |
| [**setCommunityChannelFreezeList**](CommunityChannelModerationApi.md#setCommunityChannelFreezeList) | **POST** /v4/community-channel/freeze-list/set | Set community channel freeze list |


<a id="addCommunityChannelAllowedSenderList"></a>
# **addCommunityChannelAllowedSenderList**
> CodeOnlyResponse addCommunityChannelAllowedSenderList(communityChannelAllowedSenderListUpdateRequest)

Add community channel allowed sender list

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelModerationApi apiInstance = new CommunityChannelModerationApi(defaultClient);
    
    CommunityChannelAllowedSenderListUpdateRequest communityChannelAllowedSenderListUpdateRequest = new CommunityChannelAllowedSenderListUpdateRequest(); // CommunityChannelAllowedSenderListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addCommunityChannelAllowedSenderList(communityChannelAllowedSenderListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelModerationApi#addCommunityChannelAllowedSenderList");
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
| **communityChannelAllowedSenderListUpdateRequest** | [**CommunityChannelAllowedSenderListUpdateRequest**](CommunityChannelAllowedSenderListUpdateRequest.md)|  | |

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

<a id="addCommunityChannelMutedUsers"></a>
# **addCommunityChannelMutedUsers**
> CodeOnlyResponse addCommunityChannelMutedUsers(communityChannelMuteListAddRequest)

Add community-channel muted users

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelModerationApi apiInstance = new CommunityChannelModerationApi(defaultClient);
    
    CommunityChannelMuteListAddRequest communityChannelMuteListAddRequest = new CommunityChannelMuteListAddRequest(); // CommunityChannelMuteListAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addCommunityChannelMutedUsers(communityChannelMuteListAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelModerationApi#addCommunityChannelMutedUsers");
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
| **communityChannelMuteListAddRequest** | [**CommunityChannelMuteListAddRequest**](CommunityChannelMuteListAddRequest.md)|  | |

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

<a id="getCommunityChannelFreezeList"></a>
# **getCommunityChannelFreezeList**
> CommunityChannelFreezeListGetResponse getCommunityChannelFreezeList(communityChannelFreezeListGetRequest)

Get community channel freeze status

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelModerationApi apiInstance = new CommunityChannelModerationApi(defaultClient);
    
    CommunityChannelFreezeListGetRequest communityChannelFreezeListGetRequest = new CommunityChannelFreezeListGetRequest(); // CommunityChannelFreezeListGetRequest | 
    try {
      CommunityChannelFreezeListGetResponse result = apiInstance.getCommunityChannelFreezeList(communityChannelFreezeListGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelModerationApi#getCommunityChannelFreezeList");
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
| **communityChannelFreezeListGetRequest** | [**CommunityChannelFreezeListGetRequest**](CommunityChannelFreezeListGetRequest.md)|  | |

### Return type

[**CommunityChannelFreezeListGetResponse**](CommunityChannelFreezeListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listCommunityChannelAllowedSenderList"></a>
# **listCommunityChannelAllowedSenderList**
> CommunityChannelAllowedSenderListGetResponse listCommunityChannelAllowedSenderList(communityChannelAllowedSenderListGetRequest)

List community channel allowed sender list

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelModerationApi apiInstance = new CommunityChannelModerationApi(defaultClient);
    
    CommunityChannelAllowedSenderListGetRequest communityChannelAllowedSenderListGetRequest = new CommunityChannelAllowedSenderListGetRequest(); // CommunityChannelAllowedSenderListGetRequest | 
    try {
      CommunityChannelAllowedSenderListGetResponse result = apiInstance.listCommunityChannelAllowedSenderList(communityChannelAllowedSenderListGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelModerationApi#listCommunityChannelAllowedSenderList");
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
| **communityChannelAllowedSenderListGetRequest** | [**CommunityChannelAllowedSenderListGetRequest**](CommunityChannelAllowedSenderListGetRequest.md)|  | |

### Return type

[**CommunityChannelAllowedSenderListGetResponse**](CommunityChannelAllowedSenderListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listCommunityChannelMutedUsers"></a>
# **listCommunityChannelMutedUsers**
> CommunityChannelMuteListGetResponse listCommunityChannelMutedUsers(communityChannelMuteListGetRequest)

List community-channel muted users

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelModerationApi apiInstance = new CommunityChannelModerationApi(defaultClient);
    
    CommunityChannelMuteListGetRequest communityChannelMuteListGetRequest = new CommunityChannelMuteListGetRequest(); // CommunityChannelMuteListGetRequest | 
    try {
      CommunityChannelMuteListGetResponse result = apiInstance.listCommunityChannelMutedUsers(communityChannelMuteListGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelModerationApi#listCommunityChannelMutedUsers");
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
| **communityChannelMuteListGetRequest** | [**CommunityChannelMuteListGetRequest**](CommunityChannelMuteListGetRequest.md)|  | |

### Return type

[**CommunityChannelMuteListGetResponse**](CommunityChannelMuteListGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="removeCommunityChannelAllowedSenderList"></a>
# **removeCommunityChannelAllowedSenderList**
> CodeOnlyResponse removeCommunityChannelAllowedSenderList(communityChannelAllowedSenderListUpdateRequest)

Remove community channel allowed sender list

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelModerationApi apiInstance = new CommunityChannelModerationApi(defaultClient);
    
    CommunityChannelAllowedSenderListUpdateRequest communityChannelAllowedSenderListUpdateRequest = new CommunityChannelAllowedSenderListUpdateRequest(); // CommunityChannelAllowedSenderListUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeCommunityChannelAllowedSenderList(communityChannelAllowedSenderListUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelModerationApi#removeCommunityChannelAllowedSenderList");
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
| **communityChannelAllowedSenderListUpdateRequest** | [**CommunityChannelAllowedSenderListUpdateRequest**](CommunityChannelAllowedSenderListUpdateRequest.md)|  | |

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

<a id="removeCommunityChannelMutedUsers"></a>
# **removeCommunityChannelMutedUsers**
> CodeOnlyResponse removeCommunityChannelMutedUsers(communityChannelMuteListRemoveRequest)

Remove community-channel muted users

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelModerationApi apiInstance = new CommunityChannelModerationApi(defaultClient);
    
    CommunityChannelMuteListRemoveRequest communityChannelMuteListRemoveRequest = new CommunityChannelMuteListRemoveRequest(); // CommunityChannelMuteListRemoveRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeCommunityChannelMutedUsers(communityChannelMuteListRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelModerationApi#removeCommunityChannelMutedUsers");
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
| **communityChannelMuteListRemoveRequest** | [**CommunityChannelMuteListRemoveRequest**](CommunityChannelMuteListRemoveRequest.md)|  | |

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

<a id="setCommunityChannelFreezeList"></a>
# **setCommunityChannelFreezeList**
> CodeOnlyResponse setCommunityChannelFreezeList(communityChannelFreezeListSetRequest)

Set community channel freeze list

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelModerationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelModerationApi apiInstance = new CommunityChannelModerationApi(defaultClient);
    
    CommunityChannelFreezeListSetRequest communityChannelFreezeListSetRequest = new CommunityChannelFreezeListSetRequest(); // CommunityChannelFreezeListSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setCommunityChannelFreezeList(communityChannelFreezeListSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelModerationApi#setCommunityChannelFreezeList");
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
| **communityChannelFreezeListSetRequest** | [**CommunityChannelFreezeListSetRequest**](CommunityChannelFreezeListSetRequest.md)|  | |

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

