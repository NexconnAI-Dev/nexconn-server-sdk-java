# MessageManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**broadcastOpenChannelMessage**](MessageManagementApi.md#broadcastOpenChannelMessage) | **POST** /v4/open-channel/message/broadcast | Broadcast to all open channels |
| [**deleteChannelMessageHistory**](MessageManagementApi.md#deleteChannelMessageHistory) | **POST** /v4/channel/message/history/delete | Delete server-side channel message history |
| [**deleteChannelTypeMessageMetadata**](MessageManagementApi.md#deleteChannelTypeMessageMetadata) | **POST** /v4/channel-type/message/metadata/delete | Delete message metadata |
| [**deleteCommunityChannelMessageMetadata**](MessageManagementApi.md#deleteCommunityChannelMessageMetadata) | **POST** /v4/community-channel/message/metadata/delete | Delete community-channel message metadata keys |
| [**deleteMessage**](MessageManagementApi.md#deleteMessage) | **POST** /v4/message/delete | Delete a message (recall) |
| [**listChannelTypeMessageMetadata**](MessageManagementApi.md#listChannelTypeMessageMetadata) | **POST** /v4/channel-type/message/metadata/list | Get message metadata |
| [**listCommunityChannelMessageMetadata**](MessageManagementApi.md#listCommunityChannelMessageMetadata) | **POST** /v4/community-channel/message/metadata/list | List community-channel message metadata |
| [**sendCommunityChannelMessage**](MessageManagementApi.md#sendCommunityChannelMessage) | **POST** /v4/community-channel/message/send | Send a community channel message |
| [**sendDirectChannelMessage**](MessageManagementApi.md#sendDirectChannelMessage) | **POST** /v4/direct-channel/message/send | Send a direct message |
| [**sendDirectChannelStreamMessage**](MessageManagementApi.md#sendDirectChannelStreamMessage) | **POST** /v4/direct-channel/message/stream/send | Send a direct channel stream message |
| [**sendGroupChannelMessage**](MessageManagementApi.md#sendGroupChannelMessage) | **POST** /v4/group-channel/message/send | Send a group message |
| [**sendGroupChannelStreamMessage**](MessageManagementApi.md#sendGroupChannelStreamMessage) | **POST** /v4/group-channel/message/stream/send | Send a group channel stream message |
| [**sendOpenChannelMessage**](MessageManagementApi.md#sendOpenChannelMessage) | **POST** /v4/open-channel/message/send | Send an open channel message |
| [**setChannelTypeMessageMetadata**](MessageManagementApi.md#setChannelTypeMessageMetadata) | **POST** /v4/channel-type/message/metadata/set | Set message metadata |
| [**setCommunityChannelMessageMetadata**](MessageManagementApi.md#setCommunityChannelMessageMetadata) | **POST** /v4/community-channel/message/metadata/set | Set community-channel message metadata |
| [**updateCommunityChannelMessage**](MessageManagementApi.md#updateCommunityChannelMessage) | **POST** /v4/community-channel/message/update | Update community-channel message |
| [**updateDirectChannelMessage**](MessageManagementApi.md#updateDirectChannelMessage) | **POST** /v4/direct-channel/message/update | Update direct-channel message |
| [**updateGroupChannelMessage**](MessageManagementApi.md#updateGroupChannelMessage) | **POST** /v4/group-channel/message/update | Update group-channel message |


<a id="broadcastOpenChannelMessage"></a>
# **broadcastOpenChannelMessage**
> CodeOnlyResponse broadcastOpenChannelMessage(openChannelBroadcastRequest)

Broadcast to all open channels

Rate limit: 1/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    OpenChannelBroadcastRequest openChannelBroadcastRequest = new OpenChannelBroadcastRequest(); // OpenChannelBroadcastRequest | 
    try {
      CodeOnlyResponse result = apiInstance.broadcastOpenChannelMessage(openChannelBroadcastRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#broadcastOpenChannelMessage");
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
| **openChannelBroadcastRequest** | [**OpenChannelBroadcastRequest**](OpenChannelBroadcastRequest.md)|  | |

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

<a id="deleteChannelMessageHistory"></a>
# **deleteChannelMessageHistory**
> CodeOnlyResponse deleteChannelMessageHistory(channelMessageHistoryDeleteRequest)

Delete server-side channel message history

Rate limit: 100/sec. Server path &#x60;/v4/channel/message/history/delete&#x60; (&#x60;HistoryCleanInput&#x60;).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    ChannelMessageHistoryDeleteRequest channelMessageHistoryDeleteRequest = new ChannelMessageHistoryDeleteRequest(); // ChannelMessageHistoryDeleteRequest | 
    try {
      CodeOnlyResponse result = apiInstance.deleteChannelMessageHistory(channelMessageHistoryDeleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#deleteChannelMessageHistory");
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
| **channelMessageHistoryDeleteRequest** | [**ChannelMessageHistoryDeleteRequest**](ChannelMessageHistoryDeleteRequest.md)|  | |

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

<a id="deleteChannelTypeMessageMetadata"></a>
# **deleteChannelTypeMessageMetadata**
> CodeOnlyResponse deleteChannelTypeMessageMetadata(channelTypeMessageMetadataDeleteRequest)

Delete message metadata

Rate limit: 100/sec (max 20 for group messages).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    ChannelTypeMessageMetadataDeleteRequest channelTypeMessageMetadataDeleteRequest = new ChannelTypeMessageMetadataDeleteRequest(); // ChannelTypeMessageMetadataDeleteRequest | 
    try {
      CodeOnlyResponse result = apiInstance.deleteChannelTypeMessageMetadata(channelTypeMessageMetadataDeleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#deleteChannelTypeMessageMetadata");
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
| **channelTypeMessageMetadataDeleteRequest** | [**ChannelTypeMessageMetadataDeleteRequest**](ChannelTypeMessageMetadataDeleteRequest.md)|  | |

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

<a id="deleteCommunityChannelMessageMetadata"></a>
# **deleteCommunityChannelMessageMetadata**
> CodeOnlyResponse deleteCommunityChannelMessageMetadata(communityChannelMessageMetadataDeleteRequest)

Delete community-channel message metadata keys

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    CommunityChannelMessageMetadataDeleteRequest communityChannelMessageMetadataDeleteRequest = new CommunityChannelMessageMetadataDeleteRequest(); // CommunityChannelMessageMetadataDeleteRequest | 
    try {
      CodeOnlyResponse result = apiInstance.deleteCommunityChannelMessageMetadata(communityChannelMessageMetadataDeleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#deleteCommunityChannelMessageMetadata");
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
| **communityChannelMessageMetadataDeleteRequest** | [**CommunityChannelMessageMetadataDeleteRequest**](CommunityChannelMessageMetadataDeleteRequest.md)|  | |

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

<a id="deleteMessage"></a>
# **deleteMessage**
> CodeOnlyResponse deleteMessage(messageDeleteRequest)

Delete a message (recall)

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    MessageDeleteRequest messageDeleteRequest = new MessageDeleteRequest(); // MessageDeleteRequest | 
    try {
      CodeOnlyResponse result = apiInstance.deleteMessage(messageDeleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#deleteMessage");
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
| **messageDeleteRequest** | [**MessageDeleteRequest**](MessageDeleteRequest.md)|  | |

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

<a id="listChannelTypeMessageMetadata"></a>
# **listChannelTypeMessageMetadata**
> ChannelTypeMessageMetadataListResponse listChannelTypeMessageMetadata(channelTypeMessageMetadataListRequest)

Get message metadata

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    ChannelTypeMessageMetadataListRequest channelTypeMessageMetadataListRequest = new ChannelTypeMessageMetadataListRequest(); // ChannelTypeMessageMetadataListRequest | 
    try {
      ChannelTypeMessageMetadataListResponse result = apiInstance.listChannelTypeMessageMetadata(channelTypeMessageMetadataListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#listChannelTypeMessageMetadata");
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
| **channelTypeMessageMetadataListRequest** | [**ChannelTypeMessageMetadataListRequest**](ChannelTypeMessageMetadataListRequest.md)|  | |

### Return type

[**ChannelTypeMessageMetadataListResponse**](ChannelTypeMessageMetadataListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listCommunityChannelMessageMetadata"></a>
# **listCommunityChannelMessageMetadata**
> CommunityChannelMessageMetadataListResponse listCommunityChannelMessageMetadata(communityChannelMessageMetadataListRequest)

List community-channel message metadata

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    CommunityChannelMessageMetadataListRequest communityChannelMessageMetadataListRequest = new CommunityChannelMessageMetadataListRequest(); // CommunityChannelMessageMetadataListRequest | 
    try {
      CommunityChannelMessageMetadataListResponse result = apiInstance.listCommunityChannelMessageMetadata(communityChannelMessageMetadataListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#listCommunityChannelMessageMetadata");
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
| **communityChannelMessageMetadataListRequest** | [**CommunityChannelMessageMetadataListRequest**](CommunityChannelMessageMetadataListRequest.md)|  | |

### Return type

[**CommunityChannelMessageMetadataListResponse**](CommunityChannelMessageMetadataListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="sendCommunityChannelMessage"></a>
# **sendCommunityChannelMessage**
> ChannelMessageSendResponse sendCommunityChannelMessage(communityChannelMessageSendRequest)

Send a community channel message

Rate limit: 100/sec (by target group count); 20/sec per channel.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    CommunityChannelMessageSendRequest communityChannelMessageSendRequest = new CommunityChannelMessageSendRequest(); // CommunityChannelMessageSendRequest | 
    try {
      ChannelMessageSendResponse result = apiInstance.sendCommunityChannelMessage(communityChannelMessageSendRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#sendCommunityChannelMessage");
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
| **communityChannelMessageSendRequest** | [**CommunityChannelMessageSendRequest**](CommunityChannelMessageSendRequest.md)|  | |

### Return type

[**ChannelMessageSendResponse**](ChannelMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="sendDirectChannelMessage"></a>
# **sendDirectChannelMessage**
> UserMessageSendResponse sendDirectChannelMessage(directChannelMessageSendRequest)

Send a direct message

Rate limit: 6,000 msgs/min (by recipient count).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    DirectChannelMessageSendRequest directChannelMessageSendRequest = new DirectChannelMessageSendRequest(); // DirectChannelMessageSendRequest | 
    try {
      UserMessageSendResponse result = apiInstance.sendDirectChannelMessage(directChannelMessageSendRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#sendDirectChannelMessage");
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
| **directChannelMessageSendRequest** | [**DirectChannelMessageSendRequest**](DirectChannelMessageSendRequest.md)|  | |

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

<a id="sendDirectChannelStreamMessage"></a>
# **sendDirectChannelStreamMessage**
> StreamMessageSendResponse sendDirectChannelStreamMessage(directChannelStreamMessageSendRequest)

Send a direct channel stream message

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    DirectChannelStreamMessageSendRequest directChannelStreamMessageSendRequest = new DirectChannelStreamMessageSendRequest(); // DirectChannelStreamMessageSendRequest | 
    try {
      StreamMessageSendResponse result = apiInstance.sendDirectChannelStreamMessage(directChannelStreamMessageSendRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#sendDirectChannelStreamMessage");
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
| **directChannelStreamMessageSendRequest** | [**DirectChannelStreamMessageSendRequest**](DirectChannelStreamMessageSendRequest.md)|  | |

### Return type

[**StreamMessageSendResponse**](StreamMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="sendGroupChannelMessage"></a>
# **sendGroupChannelMessage**
> ChannelMessageSendResponse sendGroupChannelMessage(groupChannelMessageSendRequest)

Send a group message

Rate limit: 20/sec (by target group count).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    GroupChannelMessageSendRequest groupChannelMessageSendRequest = new GroupChannelMessageSendRequest(); // GroupChannelMessageSendRequest | 
    try {
      ChannelMessageSendResponse result = apiInstance.sendGroupChannelMessage(groupChannelMessageSendRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#sendGroupChannelMessage");
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
| **groupChannelMessageSendRequest** | [**GroupChannelMessageSendRequest**](GroupChannelMessageSendRequest.md)|  | |

### Return type

[**ChannelMessageSendResponse**](ChannelMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="sendGroupChannelStreamMessage"></a>
# **sendGroupChannelStreamMessage**
> StreamMessageSendResponse sendGroupChannelStreamMessage(groupChannelStreamMessageSendRequest)

Send a group channel stream message

Rate limit: 100/sec.

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    GroupChannelStreamMessageSendRequest groupChannelStreamMessageSendRequest = new GroupChannelStreamMessageSendRequest(); // GroupChannelStreamMessageSendRequest | 
    try {
      StreamMessageSendResponse result = apiInstance.sendGroupChannelStreamMessage(groupChannelStreamMessageSendRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#sendGroupChannelStreamMessage");
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
| **groupChannelStreamMessageSendRequest** | [**GroupChannelStreamMessageSendRequest**](GroupChannelStreamMessageSendRequest.md)|  | |

### Return type

[**StreamMessageSendResponse**](StreamMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="sendOpenChannelMessage"></a>
# **sendOpenChannelMessage**
> ChannelMessageSendResponse sendOpenChannelMessage(openChannelMessageSendRequest)

Send an open channel message

Rate limit: 100/sec (by target open channel count).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    OpenChannelMessageSendRequest openChannelMessageSendRequest = new OpenChannelMessageSendRequest(); // OpenChannelMessageSendRequest | 
    try {
      ChannelMessageSendResponse result = apiInstance.sendOpenChannelMessage(openChannelMessageSendRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#sendOpenChannelMessage");
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
| **openChannelMessageSendRequest** | [**OpenChannelMessageSendRequest**](OpenChannelMessageSendRequest.md)|  | |

### Return type

[**ChannelMessageSendResponse**](ChannelMessageSendResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="setChannelTypeMessageMetadata"></a>
# **setChannelTypeMessageMetadata**
> CodeOnlyResponse setChannelTypeMessageMetadata(messageMetadataSetRequest)

Set message metadata

Rate limit: 100/sec (max 20 for group messages).

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    MessageMetadataSetRequest messageMetadataSetRequest = new MessageMetadataSetRequest(); // MessageMetadataSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setChannelTypeMessageMetadata(messageMetadataSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#setChannelTypeMessageMetadata");
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
| **messageMetadataSetRequest** | [**MessageMetadataSetRequest**](MessageMetadataSetRequest.md)|  | |

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

<a id="setCommunityChannelMessageMetadata"></a>
# **setCommunityChannelMessageMetadata**
> CodeOnlyResponse setCommunityChannelMessageMetadata(communityChannelMessageMetadataSetRequest)

Set community-channel message metadata

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    CommunityChannelMessageMetadataSetRequest communityChannelMessageMetadataSetRequest = new CommunityChannelMessageMetadataSetRequest(); // CommunityChannelMessageMetadataSetRequest | 
    try {
      CodeOnlyResponse result = apiInstance.setCommunityChannelMessageMetadata(communityChannelMessageMetadataSetRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#setCommunityChannelMessageMetadata");
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
| **communityChannelMessageMetadataSetRequest** | [**CommunityChannelMessageMetadataSetRequest**](CommunityChannelMessageMetadataSetRequest.md)|  | |

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

<a id="updateCommunityChannelMessage"></a>
# **updateCommunityChannelMessage**
> CodeOnlyResponse updateCommunityChannelMessage(communityChannelMessageUpdateRequest)

Update community-channel message

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    CommunityChannelMessageUpdateRequest communityChannelMessageUpdateRequest = new CommunityChannelMessageUpdateRequest(); // CommunityChannelMessageUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.updateCommunityChannelMessage(communityChannelMessageUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#updateCommunityChannelMessage");
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
| **communityChannelMessageUpdateRequest** | [**CommunityChannelMessageUpdateRequest**](CommunityChannelMessageUpdateRequest.md)|  | |

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

<a id="updateDirectChannelMessage"></a>
# **updateDirectChannelMessage**
> CodeOnlyResponse updateDirectChannelMessage(directChannelMessageUpdateRequest)

Update direct-channel message

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    DirectChannelMessageUpdateRequest directChannelMessageUpdateRequest = new DirectChannelMessageUpdateRequest(); // DirectChannelMessageUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.updateDirectChannelMessage(directChannelMessageUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#updateDirectChannelMessage");
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
| **directChannelMessageUpdateRequest** | [**DirectChannelMessageUpdateRequest**](DirectChannelMessageUpdateRequest.md)|  | |

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

<a id="updateGroupChannelMessage"></a>
# **updateGroupChannelMessage**
> CodeOnlyResponse updateGroupChannelMessage(groupChannelMessageUpdateRequest)

Update group-channel message

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.MessageManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    MessageManagementApi apiInstance = new MessageManagementApi(defaultClient);
    
    GroupChannelMessageUpdateRequest groupChannelMessageUpdateRequest = new GroupChannelMessageUpdateRequest(); // GroupChannelMessageUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.updateGroupChannelMessage(groupChannelMessageUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MessageManagementApi#updateGroupChannelMessage");
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
| **groupChannelMessageUpdateRequest** | [**GroupChannelMessageUpdateRequest**](GroupChannelMessageUpdateRequest.md)|  | |

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

