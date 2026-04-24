# ChannelManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addTagToChannels**](ChannelManagementApi.md#addTagToChannels) | **POST** /v4/channel/tag/add | Add tag to channel |
| [**addUserChannelTags**](ChannelManagementApi.md#addUserChannelTags) | **POST** /v4/user/channel/tag/add | Add user channel tag |
| [**getChannelAttribute**](ChannelManagementApi.md#getChannelAttribute) | **POST** /v4/channel/attribute/get | Get channel attributes |
| [**getChannelPushNotification**](ChannelManagementApi.md#getChannelPushNotification) | **POST** /v4/channel/push/get | Get channel DND |
| [**getChannelTypeNotification**](ChannelManagementApi.md#getChannelTypeNotification) | **POST** /v4/channel-type/push/get | Get DND by channel type |
| [**listChannelsByTag**](ChannelManagementApi.md#listChannelsByTag) | **POST** /v4/channel/tag/list | Get channels by tag |
| [**listUserChannelTags**](ChannelManagementApi.md#listUserChannelTags) | **POST** /v4/user/channel/tag/list | List user channel tags |
| [**removeTagFromChannels**](ChannelManagementApi.md#removeTagFromChannels) | **POST** /v4/channel/tag/delete | Remove tag from channel |
| [**removeUserChannelTags**](ChannelManagementApi.md#removeUserChannelTags) | **POST** /v4/user/channel/tag/remove | Remove user channel tag |
| [**setChannelPin**](ChannelManagementApi.md#setChannelPin) | **POST** /v4/channel/pin/set | Pin a channel |
| [**setChannelPushNotification**](ChannelManagementApi.md#setChannelPushNotification) | **POST** /v4/channel/push/set | Set channel DND |
| [**setChannelTypeNotification**](ChannelManagementApi.md#setChannelTypeNotification) | **POST** /v4/channel-type/push/set | Set DND by channel type |


<a id="addTagToChannels"></a>
# **addTagToChannels**
> CodeOnlyResponse addTagToChannels(channelTagAddRequest)

Add tag to channel

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    ChannelTagAddRequest channelTagAddRequest = new ChannelTagAddRequest(); // ChannelTagAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addTagToChannels(channelTagAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#addTagToChannels");
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
| **channelTagAddRequest** | [**ChannelTagAddRequest**](ChannelTagAddRequest.md)|  | |

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

<a id="addUserChannelTags"></a>
# **addUserChannelTags**
> CodeOnlyResponse addUserChannelTags(userChannelTagAddRequest)

Add user channel tag

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    UserChannelTagAddRequest userChannelTagAddRequest = new UserChannelTagAddRequest(); // UserChannelTagAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addUserChannelTags(userChannelTagAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#addUserChannelTags");
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
| **userChannelTagAddRequest** | [**UserChannelTagAddRequest**](UserChannelTagAddRequest.md)|  | |

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

<a id="getChannelAttribute"></a>
# **getChannelAttribute**
> ChannelAttributeGetResponse getChannelAttribute(channelAttributeGetRequest)

Get channel attributes

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    ChannelAttributeGetRequest channelAttributeGetRequest = new ChannelAttributeGetRequest(); // ChannelAttributeGetRequest | 
    try {
      ChannelAttributeGetResponse result = apiInstance.getChannelAttribute(channelAttributeGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#getChannelAttribute");
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
| **channelAttributeGetRequest** | [**ChannelAttributeGetRequest**](ChannelAttributeGetRequest.md)|  | |

### Return type

[**ChannelAttributeGetResponse**](ChannelAttributeGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getChannelPushNotification"></a>
# **getChannelPushNotification**
> ChannelPushGetResponse getChannelPushNotification(channelPushGetRequest)

Get channel DND

Rate limit: 100/sec. The public endpoint list currently publishes this capability as &#x60;/v4/channel/notification/get&#x60;.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    ChannelPushGetRequest channelPushGetRequest = new ChannelPushGetRequest(); // ChannelPushGetRequest | 
    try {
      ChannelPushGetResponse result = apiInstance.getChannelPushNotification(channelPushGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#getChannelPushNotification");
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
| **channelPushGetRequest** | [**ChannelPushGetRequest**](ChannelPushGetRequest.md)|  | |

### Return type

[**ChannelPushGetResponse**](ChannelPushGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getChannelTypeNotification"></a>
# **getChannelTypeNotification**
> ChannelTypeNotificationGetResponse getChannelTypeNotification(channelTypeNotificationGetRequest)

Get DND by channel type

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    ChannelTypeNotificationGetRequest channelTypeNotificationGetRequest = new ChannelTypeNotificationGetRequest(); // ChannelTypeNotificationGetRequest | 
    try {
      ChannelTypeNotificationGetResponse result = apiInstance.getChannelTypeNotification(channelTypeNotificationGetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#getChannelTypeNotification");
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
| **channelTypeNotificationGetRequest** | [**ChannelTypeNotificationGetRequest**](ChannelTypeNotificationGetRequest.md)|  | |

### Return type

[**ChannelTypeNotificationGetResponse**](ChannelTypeNotificationGetResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listChannelsByTag"></a>
# **listChannelsByTag**
> ChannelTagListResponse listChannelsByTag(channelTagListRequest)

Get channels by tag

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    ChannelTagListRequest channelTagListRequest = new ChannelTagListRequest(); // ChannelTagListRequest | 
    try {
      ChannelTagListResponse result = apiInstance.listChannelsByTag(channelTagListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#listChannelsByTag");
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
| **channelTagListRequest** | [**ChannelTagListRequest**](ChannelTagListRequest.md)|  | |

### Return type

[**ChannelTagListResponse**](ChannelTagListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listUserChannelTags"></a>
# **listUserChannelTags**
> UserChannelTagListResponse listUserChannelTags(userChannelTagListRequest)

List user channel tags

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    UserChannelTagListRequest userChannelTagListRequest = new UserChannelTagListRequest(); // UserChannelTagListRequest | 
    try {
      UserChannelTagListResponse result = apiInstance.listUserChannelTags(userChannelTagListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#listUserChannelTags");
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
| **userChannelTagListRequest** | [**UserChannelTagListRequest**](UserChannelTagListRequest.md)|  | |

### Return type

[**UserChannelTagListResponse**](UserChannelTagListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="removeTagFromChannels"></a>
# **removeTagFromChannels**
> CodeOnlyResponse removeTagFromChannels(channelTagRemoveRequest)

Remove tag from channel

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    ChannelTagRemoveRequest channelTagRemoveRequest = new ChannelTagRemoveRequest(); // ChannelTagRemoveRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeTagFromChannels(channelTagRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#removeTagFromChannels");
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
| **channelTagRemoveRequest** | [**ChannelTagRemoveRequest**](ChannelTagRemoveRequest.md)|  | |

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

<a id="removeUserChannelTags"></a>
# **removeUserChannelTags**
> CodeOnlyResponse removeUserChannelTags(userChannelTagRemoveRequest)

Remove user channel tag

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    UserChannelTagRemoveRequest userChannelTagRemoveRequest = new UserChannelTagRemoveRequest(); // UserChannelTagRemoveRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeUserChannelTags(userChannelTagRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#removeUserChannelTags");
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
| **userChannelTagRemoveRequest** | [**UserChannelTagRemoveRequest**](UserChannelTagRemoveRequest.md)|  | |

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

<a id="setChannelPin"></a>
# **setChannelPin**
> CodeOnlyResponse setChannelPin(channelPinSetRequest)

Pin a channel

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    ChannelPinSetRequest channelPinSetRequest = new ChannelPinSetRequest(); // ChannelPinSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setChannelPin(channelPinSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#setChannelPin");
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
| **channelPinSetRequest** | [**ChannelPinSetRequest**](ChannelPinSetRequest.md)|  | |

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

<a id="setChannelPushNotification"></a>
# **setChannelPushNotification**
> CodeOnlyResponse setChannelPushNotification(channelPushSetRequest)

Set channel DND

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    ChannelPushSetRequest channelPushSetRequest = new ChannelPushSetRequest(); // ChannelPushSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setChannelPushNotification(channelPushSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#setChannelPushNotification");
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
| **channelPushSetRequest** | [**ChannelPushSetRequest**](ChannelPushSetRequest.md)|  | |

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

<a id="setChannelTypeNotification"></a>
# **setChannelTypeNotification**
> CodeOnlyResponse setChannelTypeNotification(channelTypeNotificationSetRequest)

Set DND by channel type

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.ChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    ChannelManagementApi apiInstance = new ChannelManagementApi(defaultClient);
    
    ChannelTypeNotificationSetRequest channelTypeNotificationSetRequest = new ChannelTypeNotificationSetRequest(); // ChannelTypeNotificationSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setChannelTypeNotification(channelTypeNotificationSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChannelManagementApi#setChannelTypeNotification");
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
| **channelTypeNotificationSetRequest** | [**ChannelTypeNotificationSetRequest**](ChannelTypeNotificationSetRequest.md)|  | |

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

