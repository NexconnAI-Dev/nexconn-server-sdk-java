# SystemMessagesApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**broadcastMessageOnline**](SystemMessagesApi.md#broadcastMessageOnline) | **POST** /v4/system-channel/message/broadcast-online | Broadcast to online users |
| [**broadcastSystemChannelMessage**](SystemMessagesApi.md#broadcastSystemChannelMessage) | **POST** /v4/system-channel/message/broadcast-all | Broadcast to all users (persistent) |
| [**deleteBroadcastMessage**](SystemMessagesApi.md#deleteBroadcastMessage) | **POST** /v4/system-channel/message/broadcast/delete | Recall broadcast to all users |
| [**sendSystemChannelMessage**](SystemMessagesApi.md#sendSystemChannelMessage) | **POST** /v4/system-channel/message/send | Send a system message |
| [**sendSystemChannelPushByPackage**](SystemMessagesApi.md#sendSystemChannelPushByPackage) | **POST** /v4/system-channel/app-package-users/send | Push by app package name |
| [**sendSystemChannelPushByTag**](SystemMessagesApi.md#sendSystemChannelPushByTag) | **POST** /v4/system-channel/tagged-users/send | Push to tagged users |


<a id="broadcastMessageOnline"></a>
# **broadcastMessageOnline**
> SingleMessageIdResponse broadcastMessageOnline(systemChannelBroadcastOnlineRequest)

Broadcast to online users

Rate limit: 60/min.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.SystemMessagesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    SystemMessagesApi apiInstance = new SystemMessagesApi(defaultClient);
    
    SystemChannelBroadcastOnlineRequest systemChannelBroadcastOnlineRequest = new SystemChannelBroadcastOnlineRequest(); // SystemChannelBroadcastOnlineRequest | 
    try {
      SingleMessageIdResponse result = apiInstance.broadcastMessageOnline(systemChannelBroadcastOnlineRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemMessagesApi#broadcastMessageOnline");
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
| **systemChannelBroadcastOnlineRequest** | [**SystemChannelBroadcastOnlineRequest**](SystemChannelBroadcastOnlineRequest.md)|  | |

### Return type

[**SingleMessageIdResponse**](SingleMessageIdResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="broadcastSystemChannelMessage"></a>
# **broadcastSystemChannelMessage**
> SingleMessageIdResponse broadcastSystemChannelMessage(systemChannelBroadcastAllRequest)

Broadcast to all users (persistent)

Rate limit: 2/hour, 3/day.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.SystemMessagesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    SystemMessagesApi apiInstance = new SystemMessagesApi(defaultClient);
    
    SystemChannelBroadcastAllRequest systemChannelBroadcastAllRequest = new SystemChannelBroadcastAllRequest(); // SystemChannelBroadcastAllRequest | 
    try {
      SingleMessageIdResponse result = apiInstance.broadcastSystemChannelMessage(systemChannelBroadcastAllRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemMessagesApi#broadcastSystemChannelMessage");
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
| **systemChannelBroadcastAllRequest** | [**SystemChannelBroadcastAllRequest**](SystemChannelBroadcastAllRequest.md)|  | |

### Return type

[**SingleMessageIdResponse**](SingleMessageIdResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="deleteBroadcastMessage"></a>
# **deleteBroadcastMessage**
> CodeOnlyResponse deleteBroadcastMessage(systemChannelBroadcastDeleteRequest)

Recall broadcast to all users

Rate limit: 2/hour, 3/day.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.SystemMessagesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    SystemMessagesApi apiInstance = new SystemMessagesApi(defaultClient);
    
    SystemChannelBroadcastDeleteRequest systemChannelBroadcastDeleteRequest = new SystemChannelBroadcastDeleteRequest(); // SystemChannelBroadcastDeleteRequest | 
    try {
      CodeOnlyResponse result = apiInstance.deleteBroadcastMessage(systemChannelBroadcastDeleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemMessagesApi#deleteBroadcastMessage");
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
| **systemChannelBroadcastDeleteRequest** | [**SystemChannelBroadcastDeleteRequest**](SystemChannelBroadcastDeleteRequest.md)|  | |

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

<a id="sendSystemChannelMessage"></a>
# **sendSystemChannelMessage**
> UserMessageSendResponse sendSystemChannelMessage(systemChannelMessageSendRequest)

Send a system message

Rate limit: 100 msgs/sec (by recipient count).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.SystemMessagesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    SystemMessagesApi apiInstance = new SystemMessagesApi(defaultClient);
    
    SystemChannelMessageSendRequest systemChannelMessageSendRequest = new SystemChannelMessageSendRequest(); // SystemChannelMessageSendRequest | 
    try {
      UserMessageSendResponse result = apiInstance.sendSystemChannelMessage(systemChannelMessageSendRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemMessagesApi#sendSystemChannelMessage");
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
| **systemChannelMessageSendRequest** | [**SystemChannelMessageSendRequest**](SystemChannelMessageSendRequest.md)|  | |

### Return type

[**UserMessageSendResponse**](UserMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="sendSystemChannelPushByPackage"></a>
# **sendSystemChannelPushByPackage**
> SystemChannelPushResponse sendSystemChannelPushByPackage(systemChannelPushRequest)

Push by app package name

Rate limit: 2/hour, 3/day (shared).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.SystemMessagesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    SystemMessagesApi apiInstance = new SystemMessagesApi(defaultClient);
    
    SystemChannelPushRequest systemChannelPushRequest = new SystemChannelPushRequest(); // SystemChannelPushRequest | 
    try {
      SystemChannelPushResponse result = apiInstance.sendSystemChannelPushByPackage(systemChannelPushRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemMessagesApi#sendSystemChannelPushByPackage");
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
| **systemChannelPushRequest** | [**SystemChannelPushRequest**](SystemChannelPushRequest.md)|  | |

### Return type

[**SystemChannelPushResponse**](SystemChannelPushResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="sendSystemChannelPushByTag"></a>
# **sendSystemChannelPushByTag**
> SystemChannelPushResponse sendSystemChannelPushByTag(systemChannelPushRequest)

Push to tagged users

Rate limit: 2/hour, 3/day (shared).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.SystemMessagesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    SystemMessagesApi apiInstance = new SystemMessagesApi(defaultClient);
    
    SystemChannelPushRequest systemChannelPushRequest = new SystemChannelPushRequest(); // SystemChannelPushRequest | 
    try {
      SystemChannelPushResponse result = apiInstance.sendSystemChannelPushByTag(systemChannelPushRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SystemMessagesApi#sendSystemChannelPushByTag");
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
| **systemChannelPushRequest** | [**SystemChannelPushRequest**](SystemChannelPushRequest.md)|  | |

### Return type

[**SystemChannelPushResponse**](SystemChannelPushResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

