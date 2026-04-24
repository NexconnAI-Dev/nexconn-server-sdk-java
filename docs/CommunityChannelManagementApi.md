# CommunityChannelManagementApi

All requests use the primary/backup domains configured by the caller.

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addCommunityChannelUserGroupUsers**](CommunityChannelManagementApi.md#addCommunityChannelUserGroupUsers) | **POST** /v4/community-channel/user-group/user/add | Add community channel user group users |
| [**addCommunityChannelUserGroups**](CommunityChannelManagementApi.md#addCommunityChannelUserGroups) | **POST** /v4/community-channel/user-group/add | Add community channel user groups |
| [**addPrivateSubchannelMembers**](CommunityChannelManagementApi.md#addPrivateSubchannelMembers) | **POST** /v4/community-channel/private-subchannel/member/add | Add private subchannel members |
| [**bindCommunityChannelUserGroup**](CommunityChannelManagementApi.md#bindCommunityChannelUserGroup) | **POST** /v4/community-channel/channel/user-group/bind | Bind community channel user group |
| [**checkCommunityChannelMemberExist**](CommunityChannelManagementApi.md#checkCommunityChannelMemberExist) | **POST** /v4/community-channel/member/exist | Check community channel member exist |
| [**createCommunityChannel**](CommunityChannelManagementApi.md#createCommunityChannel) | **POST** /v4/community-channel/create | Create community channel |
| [**createCommunitySubchannel**](CommunityChannelManagementApi.md#createCommunitySubchannel) | **POST** /v4/community-channel/subchannel/create | Create community subchannel |
| [**deleteCommunitySubchannel**](CommunityChannelManagementApi.md#deleteCommunitySubchannel) | **POST** /v4/community-channel/subchannel/delete | Delete community subchannel |
| [**dismissCommunityChannel**](CommunityChannelManagementApi.md#dismissCommunityChannel) | **POST** /v4/community-channel/dismiss | Dismiss community channel |
| [**joinCommunityChannel**](CommunityChannelManagementApi.md#joinCommunityChannel) | **POST** /v4/community-channel/join | Join community channel |
| [**listCommunityChannelHistoryMessages**](CommunityChannelManagementApi.md#listCommunityChannelHistoryMessages) | **POST** /v4/community-channel/history-message/list | List community-channel history messages |
| [**listCommunityChannelSubchannelUserGroups**](CommunityChannelManagementApi.md#listCommunityChannelSubchannelUserGroups) | **POST** /v4/community-channel/channel/user-group/list | List community channel subchannel user groups |
| [**listCommunityChannelUserGroupSubchannels**](CommunityChannelManagementApi.md#listCommunityChannelUserGroupSubchannels) | **POST** /v4/community-channel/user-group/subchannel/list | List community channel user group subchannels |
| [**listCommunityChannelUserGroups**](CommunityChannelManagementApi.md#listCommunityChannelUserGroups) | **POST** /v4/community-channel/user-group/list | List community channel user groups |
| [**listCommunityChannelUserUserGroups**](CommunityChannelManagementApi.md#listCommunityChannelUserUserGroups) | **POST** /v4/community-channel/user/user-group/list | List community channel user user groups |
| [**listCommunitySubchannels**](CommunityChannelManagementApi.md#listCommunitySubchannels) | **POST** /v4/community-channel/subchannel/list | List community subchannels |
| [**listCommunityUserSubchannels**](CommunityChannelManagementApi.md#listCommunityUserSubchannels) | **POST** /v4/community-channel/user/subchannel/list | List community user subchannels |
| [**listPrivateSubchannelMembers**](CommunityChannelManagementApi.md#listPrivateSubchannelMembers) | **POST** /v4/community-channel/private-subchannel/member/list | List private subchannel members |
| [**quitCommunityChannel**](CommunityChannelManagementApi.md#quitCommunityChannel) | **POST** /v4/community-channel/leave | Leave community channel |
| [**removeCommunityChannelUserGroupUsers**](CommunityChannelManagementApi.md#removeCommunityChannelUserGroupUsers) | **POST** /v4/community-channel/user-group/user/remove | Remove community channel user group users |
| [**removeCommunityChannelUserGroups**](CommunityChannelManagementApi.md#removeCommunityChannelUserGroups) | **POST** /v4/community-channel/user-group/remove | Delete community channel user groups |
| [**removePrivateSubchannelMembers**](CommunityChannelManagementApi.md#removePrivateSubchannelMembers) | **POST** /v4/community-channel/private-subchannel/member/remove | Remove private subchannel members |
| [**unbindCommunityChannelUserGroup**](CommunityChannelManagementApi.md#unbindCommunityChannelUserGroup) | **POST** /v4/community-channel/channel/user-group/unbind | Unbind community channel user group |
| [**updateCommunityChannelInfo**](CommunityChannelManagementApi.md#updateCommunityChannelInfo) | **POST** /v4/community-channel/update | Update community channel info |
| [**updateCommunitySubchannelType**](CommunityChannelManagementApi.md#updateCommunitySubchannelType) | **POST** /v4/community-channel/subchannel-type/update | Update community subchannel type |


<a id="addCommunityChannelUserGroupUsers"></a>
# **addCommunityChannelUserGroupUsers**
> CodeOnlyResponse addCommunityChannelUserGroupUsers(communityChannelUserGroupUsersRequest)

Add community channel user group users

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUserGroupUsersRequest communityChannelUserGroupUsersRequest = new CommunityChannelUserGroupUsersRequest(); // CommunityChannelUserGroupUsersRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addCommunityChannelUserGroupUsers(communityChannelUserGroupUsersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#addCommunityChannelUserGroupUsers");
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
| **communityChannelUserGroupUsersRequest** | [**CommunityChannelUserGroupUsersRequest**](CommunityChannelUserGroupUsersRequest.md)|  | |

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

<a id="addCommunityChannelUserGroups"></a>
# **addCommunityChannelUserGroups**
> CodeOnlyResponse addCommunityChannelUserGroups(communityChannelUserGroupAddRequest)

Add community channel user groups

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUserGroupAddRequest communityChannelUserGroupAddRequest = new CommunityChannelUserGroupAddRequest(); // CommunityChannelUserGroupAddRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addCommunityChannelUserGroups(communityChannelUserGroupAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#addCommunityChannelUserGroups");
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
| **communityChannelUserGroupAddRequest** | [**CommunityChannelUserGroupAddRequest**](CommunityChannelUserGroupAddRequest.md)|  | |

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

<a id="addPrivateSubchannelMembers"></a>
# **addPrivateSubchannelMembers**
> CodeOnlyResponse addPrivateSubchannelMembers(communityPrivateSubchannelMembersRequest)

Add private subchannel members

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityPrivateSubchannelMembersRequest communityPrivateSubchannelMembersRequest = new CommunityPrivateSubchannelMembersRequest(); // CommunityPrivateSubchannelMembersRequest | 
    try {
      CodeOnlyResponse result = apiInstance.addPrivateSubchannelMembers(communityPrivateSubchannelMembersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#addPrivateSubchannelMembers");
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
| **communityPrivateSubchannelMembersRequest** | [**CommunityPrivateSubchannelMembersRequest**](CommunityPrivateSubchannelMembersRequest.md)|  | |

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

<a id="bindCommunityChannelUserGroup"></a>
# **bindCommunityChannelUserGroup**
> CodeOnlyResponse bindCommunityChannelUserGroup(communityChannelUserGroupBindingRequest)

Bind community channel user group

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUserGroupBindingRequest communityChannelUserGroupBindingRequest = new CommunityChannelUserGroupBindingRequest(); // CommunityChannelUserGroupBindingRequest | 
    try {
      CodeOnlyResponse result = apiInstance.bindCommunityChannelUserGroup(communityChannelUserGroupBindingRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#bindCommunityChannelUserGroup");
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
| **communityChannelUserGroupBindingRequest** | [**CommunityChannelUserGroupBindingRequest**](CommunityChannelUserGroupBindingRequest.md)|  | |

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

<a id="checkCommunityChannelMemberExist"></a>
# **checkCommunityChannelMemberExist**
> CommunityChannelMemberExistResponse checkCommunityChannelMemberExist(communityChannelMemberRequest)

Check community channel member exist

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelMemberRequest communityChannelMemberRequest = new CommunityChannelMemberRequest(); // CommunityChannelMemberRequest | 
    try {
      CommunityChannelMemberExistResponse result = apiInstance.checkCommunityChannelMemberExist(communityChannelMemberRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#checkCommunityChannelMemberExist");
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
| **communityChannelMemberRequest** | [**CommunityChannelMemberRequest**](CommunityChannelMemberRequest.md)|  | |

### Return type

[**CommunityChannelMemberExistResponse**](CommunityChannelMemberExistResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="createCommunityChannel"></a>
# **createCommunityChannel**
> CodeOnlyResponse createCommunityChannel(communityChannelCreateRequest)

Create community channel

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelCreateRequest communityChannelCreateRequest = new CommunityChannelCreateRequest(); // CommunityChannelCreateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.createCommunityChannel(communityChannelCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#createCommunityChannel");
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
| **communityChannelCreateRequest** | [**CommunityChannelCreateRequest**](CommunityChannelCreateRequest.md)|  | |

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

<a id="createCommunitySubchannel"></a>
# **createCommunitySubchannel**
> CodeOnlyResponse createCommunitySubchannel(communitySubchannelCreateRequest)

Create community subchannel

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunitySubchannelCreateRequest communitySubchannelCreateRequest = new CommunitySubchannelCreateRequest(); // CommunitySubchannelCreateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.createCommunitySubchannel(communitySubchannelCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#createCommunitySubchannel");
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
| **communitySubchannelCreateRequest** | [**CommunitySubchannelCreateRequest**](CommunitySubchannelCreateRequest.md)|  | |

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

<a id="deleteCommunitySubchannel"></a>
# **deleteCommunitySubchannel**
> CodeOnlyResponse deleteCommunitySubchannel(communitySubchannelKeyRequest)

Delete community subchannel

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunitySubchannelKeyRequest communitySubchannelKeyRequest = new CommunitySubchannelKeyRequest(); // CommunitySubchannelKeyRequest | 
    try {
      CodeOnlyResponse result = apiInstance.deleteCommunitySubchannel(communitySubchannelKeyRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#deleteCommunitySubchannel");
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
| **communitySubchannelKeyRequest** | [**CommunitySubchannelKeyRequest**](CommunitySubchannelKeyRequest.md)|  | |

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

<a id="dismissCommunityChannel"></a>
# **dismissCommunityChannel**
> CodeOnlyResponse dismissCommunityChannel(communityChannelDismissRequest)

Dismiss community channel

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelDismissRequest communityChannelDismissRequest = new CommunityChannelDismissRequest(); // CommunityChannelDismissRequest | 
    try {
      CodeOnlyResponse result = apiInstance.dismissCommunityChannel(communityChannelDismissRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#dismissCommunityChannel");
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
| **communityChannelDismissRequest** | [**CommunityChannelDismissRequest**](CommunityChannelDismissRequest.md)|  | |

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

<a id="joinCommunityChannel"></a>
# **joinCommunityChannel**
> CodeOnlyResponse joinCommunityChannel(communityChannelMemberRequest)

Join community channel

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelMemberRequest communityChannelMemberRequest = new CommunityChannelMemberRequest(); // CommunityChannelMemberRequest | 
    try {
      CodeOnlyResponse result = apiInstance.joinCommunityChannel(communityChannelMemberRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#joinCommunityChannel");
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
| **communityChannelMemberRequest** | [**CommunityChannelMemberRequest**](CommunityChannelMemberRequest.md)|  | |

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

<a id="listCommunityChannelHistoryMessages"></a>
# **listCommunityChannelHistoryMessages**
> MessageHistoryResponse listCommunityChannelHistoryMessages(communityChannelHistoryMessageListRequest)

List community-channel history messages

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelHistoryMessageListRequest communityChannelHistoryMessageListRequest = new CommunityChannelHistoryMessageListRequest(); // CommunityChannelHistoryMessageListRequest | 
    try {
      MessageHistoryResponse result = apiInstance.listCommunityChannelHistoryMessages(communityChannelHistoryMessageListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#listCommunityChannelHistoryMessages");
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
| **communityChannelHistoryMessageListRequest** | [**CommunityChannelHistoryMessageListRequest**](CommunityChannelHistoryMessageListRequest.md)|  | |

### Return type

[**MessageHistoryResponse**](MessageHistoryResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listCommunityChannelSubchannelUserGroups"></a>
# **listCommunityChannelSubchannelUserGroups**
> CommunityChannelSubchannelUserGroupListResponse listCommunityChannelSubchannelUserGroups(communityChannelSubchannelUserGroupListRequest)

List community channel subchannel user groups

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelSubchannelUserGroupListRequest communityChannelSubchannelUserGroupListRequest = new CommunityChannelSubchannelUserGroupListRequest(); // CommunityChannelSubchannelUserGroupListRequest | 
    try {
      CommunityChannelSubchannelUserGroupListResponse result = apiInstance.listCommunityChannelSubchannelUserGroups(communityChannelSubchannelUserGroupListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#listCommunityChannelSubchannelUserGroups");
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
| **communityChannelSubchannelUserGroupListRequest** | [**CommunityChannelSubchannelUserGroupListRequest**](CommunityChannelSubchannelUserGroupListRequest.md)|  | |

### Return type

[**CommunityChannelSubchannelUserGroupListResponse**](CommunityChannelSubchannelUserGroupListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listCommunityChannelUserGroupSubchannels"></a>
# **listCommunityChannelUserGroupSubchannels**
> CommunityChannelUserGroupSubchannelListResponse listCommunityChannelUserGroupSubchannels(communityChannelUserGroupSubchannelListRequest)

List community channel user group subchannels

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUserGroupSubchannelListRequest communityChannelUserGroupSubchannelListRequest = new CommunityChannelUserGroupSubchannelListRequest(); // CommunityChannelUserGroupSubchannelListRequest | 
    try {
      CommunityChannelUserGroupSubchannelListResponse result = apiInstance.listCommunityChannelUserGroupSubchannels(communityChannelUserGroupSubchannelListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#listCommunityChannelUserGroupSubchannels");
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
| **communityChannelUserGroupSubchannelListRequest** | [**CommunityChannelUserGroupSubchannelListRequest**](CommunityChannelUserGroupSubchannelListRequest.md)|  | |

### Return type

[**CommunityChannelUserGroupSubchannelListResponse**](CommunityChannelUserGroupSubchannelListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listCommunityChannelUserGroups"></a>
# **listCommunityChannelUserGroups**
> CommunityChannelUserGroupListResponse listCommunityChannelUserGroups(communityChannelUserGroupListRequest)

List community channel user groups

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUserGroupListRequest communityChannelUserGroupListRequest = new CommunityChannelUserGroupListRequest(); // CommunityChannelUserGroupListRequest | 
    try {
      CommunityChannelUserGroupListResponse result = apiInstance.listCommunityChannelUserGroups(communityChannelUserGroupListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#listCommunityChannelUserGroups");
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
| **communityChannelUserGroupListRequest** | [**CommunityChannelUserGroupListRequest**](CommunityChannelUserGroupListRequest.md)|  | |

### Return type

[**CommunityChannelUserGroupListResponse**](CommunityChannelUserGroupListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listCommunityChannelUserUserGroups"></a>
# **listCommunityChannelUserUserGroups**
> CommunityChannelUserUserGroupListResponse listCommunityChannelUserUserGroups(communityChannelUserUserGroupListRequest)

List community channel user user groups

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUserUserGroupListRequest communityChannelUserUserGroupListRequest = new CommunityChannelUserUserGroupListRequest(); // CommunityChannelUserUserGroupListRequest | 
    try {
      CommunityChannelUserUserGroupListResponse result = apiInstance.listCommunityChannelUserUserGroups(communityChannelUserUserGroupListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#listCommunityChannelUserUserGroups");
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
| **communityChannelUserUserGroupListRequest** | [**CommunityChannelUserUserGroupListRequest**](CommunityChannelUserUserGroupListRequest.md)|  | |

### Return type

[**CommunityChannelUserUserGroupListResponse**](CommunityChannelUserUserGroupListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listCommunitySubchannels"></a>
# **listCommunitySubchannels**
> CommunitySubchannelListResponse listCommunitySubchannels(communitySubchannelListRequest)

List community subchannels

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunitySubchannelListRequest communitySubchannelListRequest = new CommunitySubchannelListRequest(); // CommunitySubchannelListRequest | 
    try {
      CommunitySubchannelListResponse result = apiInstance.listCommunitySubchannels(communitySubchannelListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#listCommunitySubchannels");
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
| **communitySubchannelListRequest** | [**CommunitySubchannelListRequest**](CommunitySubchannelListRequest.md)|  | |

### Return type

[**CommunitySubchannelListResponse**](CommunitySubchannelListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listCommunityUserSubchannels"></a>
# **listCommunityUserSubchannels**
> CommunityUserSubchannelListResponse listCommunityUserSubchannels(communityUserSubchannelListRequest)

List community user subchannels

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityUserSubchannelListRequest communityUserSubchannelListRequest = new CommunityUserSubchannelListRequest(); // CommunityUserSubchannelListRequest | 
    try {
      CommunityUserSubchannelListResponse result = apiInstance.listCommunityUserSubchannels(communityUserSubchannelListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#listCommunityUserSubchannels");
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
| **communityUserSubchannelListRequest** | [**CommunityUserSubchannelListRequest**](CommunityUserSubchannelListRequest.md)|  | |

### Return type

[**CommunityUserSubchannelListResponse**](CommunityUserSubchannelListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listPrivateSubchannelMembers"></a>
# **listPrivateSubchannelMembers**
> CommunityPrivateSubchannelMemberListResponse listPrivateSubchannelMembers(communityPrivateSubchannelMemberListRequest)

List private subchannel members

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityPrivateSubchannelMemberListRequest communityPrivateSubchannelMemberListRequest = new CommunityPrivateSubchannelMemberListRequest(); // CommunityPrivateSubchannelMemberListRequest | 
    try {
      CommunityPrivateSubchannelMemberListResponse result = apiInstance.listPrivateSubchannelMembers(communityPrivateSubchannelMemberListRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#listPrivateSubchannelMembers");
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
| **communityPrivateSubchannelMemberListRequest** | [**CommunityPrivateSubchannelMemberListRequest**](CommunityPrivateSubchannelMemberListRequest.md)|  | |

### Return type

[**CommunityPrivateSubchannelMemberListResponse**](CommunityPrivateSubchannelMemberListResponse.md)

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="quitCommunityChannel"></a>
# **quitCommunityChannel**
> CodeOnlyResponse quitCommunityChannel(communityChannelMemberRequest)

Leave community channel

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelMemberRequest communityChannelMemberRequest = new CommunityChannelMemberRequest(); // CommunityChannelMemberRequest | 
    try {
      CodeOnlyResponse result = apiInstance.quitCommunityChannel(communityChannelMemberRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#quitCommunityChannel");
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
| **communityChannelMemberRequest** | [**CommunityChannelMemberRequest**](CommunityChannelMemberRequest.md)|  | |

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

<a id="removeCommunityChannelUserGroupUsers"></a>
# **removeCommunityChannelUserGroupUsers**
> CodeOnlyResponse removeCommunityChannelUserGroupUsers(communityChannelUserGroupUsersRequest)

Remove community channel user group users

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUserGroupUsersRequest communityChannelUserGroupUsersRequest = new CommunityChannelUserGroupUsersRequest(); // CommunityChannelUserGroupUsersRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeCommunityChannelUserGroupUsers(communityChannelUserGroupUsersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#removeCommunityChannelUserGroupUsers");
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
| **communityChannelUserGroupUsersRequest** | [**CommunityChannelUserGroupUsersRequest**](CommunityChannelUserGroupUsersRequest.md)|  | |

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

<a id="removeCommunityChannelUserGroups"></a>
# **removeCommunityChannelUserGroups**
> CodeOnlyResponse removeCommunityChannelUserGroups(communityChannelUserGroupDeleteRequest)

Delete community channel user groups

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUserGroupDeleteRequest communityChannelUserGroupDeleteRequest = new CommunityChannelUserGroupDeleteRequest(); // CommunityChannelUserGroupDeleteRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removeCommunityChannelUserGroups(communityChannelUserGroupDeleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#removeCommunityChannelUserGroups");
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
| **communityChannelUserGroupDeleteRequest** | [**CommunityChannelUserGroupDeleteRequest**](CommunityChannelUserGroupDeleteRequest.md)|  | |

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

<a id="removePrivateSubchannelMembers"></a>
# **removePrivateSubchannelMembers**
> CodeOnlyResponse removePrivateSubchannelMembers(communityPrivateSubchannelMembersRequest)

Remove private subchannel members

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityPrivateSubchannelMembersRequest communityPrivateSubchannelMembersRequest = new CommunityPrivateSubchannelMembersRequest(); // CommunityPrivateSubchannelMembersRequest | 
    try {
      CodeOnlyResponse result = apiInstance.removePrivateSubchannelMembers(communityPrivateSubchannelMembersRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#removePrivateSubchannelMembers");
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
| **communityPrivateSubchannelMembersRequest** | [**CommunityPrivateSubchannelMembersRequest**](CommunityPrivateSubchannelMembersRequest.md)|  | |

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

<a id="unbindCommunityChannelUserGroup"></a>
# **unbindCommunityChannelUserGroup**
> CodeOnlyResponse unbindCommunityChannelUserGroup(communityChannelUserGroupBindingRequest)

Unbind community channel user group

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUserGroupBindingRequest communityChannelUserGroupBindingRequest = new CommunityChannelUserGroupBindingRequest(); // CommunityChannelUserGroupBindingRequest | 
    try {
      CodeOnlyResponse result = apiInstance.unbindCommunityChannelUserGroup(communityChannelUserGroupBindingRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#unbindCommunityChannelUserGroup");
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
| **communityChannelUserGroupBindingRequest** | [**CommunityChannelUserGroupBindingRequest**](CommunityChannelUserGroupBindingRequest.md)|  | |

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

<a id="updateCommunityChannelInfo"></a>
# **updateCommunityChannelInfo**
> CodeOnlyResponse updateCommunityChannelInfo(communityChannelUpdateRequest)

Update community channel info

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunityChannelUpdateRequest communityChannelUpdateRequest = new CommunityChannelUpdateRequest(); // CommunityChannelUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.updateCommunityChannelInfo(communityChannelUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#updateCommunityChannelInfo");
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
| **communityChannelUpdateRequest** | [**CommunityChannelUpdateRequest**](CommunityChannelUpdateRequest.md)|  | |

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

<a id="updateCommunitySubchannelType"></a>
# **updateCommunitySubchannelType**
> CodeOnlyResponse updateCommunitySubchannelType(communitySubchannelTypeUpdateRequest)

Update community subchannel type

### Example
```java
// Import classes:
import ai.nexconn.ApiClient;
import ai.nexconn.ApiException;
import ai.nexconn.Configuration;
import ai.nexconn.model.*;
import ai.nexconn.api.CommunityChannelManagementApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.sg-light-api.com");
    
    // Configure API key authorization: NexconnSignature
    ApiKeyAuth NexconnSignature = (ApiKeyAuth) defaultClient.getAuthentication("NexconnSignature");
    NexconnSignature.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //NexconnSignature.setApiKeyPrefix("Token");

    CommunityChannelManagementApi apiInstance = new CommunityChannelManagementApi(defaultClient);
    
    CommunitySubchannelTypeUpdateRequest communitySubchannelTypeUpdateRequest = new CommunitySubchannelTypeUpdateRequest(); // CommunitySubchannelTypeUpdateRequest | 
    try {
      CodeOnlyResponse result = apiInstance.updateCommunitySubchannelType(communitySubchannelTypeUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CommunityChannelManagementApi#updateCommunitySubchannelType");
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
| **communitySubchannelTypeUpdateRequest** | [**CommunitySubchannelTypeUpdateRequest**](CommunitySubchannelTypeUpdateRequest.md)|  | |

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

