# ConversationsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**conversationsAgentOnlinePingPost**](ConversationsApi.md#conversationsAgentOnlinePingPost) | **POST** /conversations/agentOnlinePing | Sets agent’s status to online for 2-3 minutes
[**conversationsMessagesIdDelete**](ConversationsApi.md#conversationsMessagesIdDelete) | **DELETE** /conversations/messages/{id} | Delete a message sent by an agent
[**conversationsMessagesIdGet**](ConversationsApi.md#conversationsMessagesIdGet) | **GET** /conversations/messages/{id} | Get a message
[**conversationsMessagesIdPut**](ConversationsApi.md#conversationsMessagesIdPut) | **PUT** /conversations/messages/{id} | Update a message sent by an agent
[**conversationsMessagesPost**](ConversationsApi.md#conversationsMessagesPost) | **POST** /conversations/messages | Send a message as an agent
[**conversationsPushedMessagesIdDelete**](ConversationsApi.md#conversationsPushedMessagesIdDelete) | **DELETE** /conversations/pushedMessages/{id} | Delete an automated message
[**conversationsPushedMessagesIdGet**](ConversationsApi.md#conversationsPushedMessagesIdGet) | **GET** /conversations/pushedMessages/{id} | Get an automated message
[**conversationsPushedMessagesIdPut**](ConversationsApi.md#conversationsPushedMessagesIdPut) | **PUT** /conversations/pushedMessages/{id} | Update an automated message
[**conversationsPushedMessagesPost**](ConversationsApi.md#conversationsPushedMessagesPost) | **POST** /conversations/pushedMessages | Send an automated message to a visitor


<a name="conversationsAgentOnlinePingPost"></a>
# **conversationsAgentOnlinePingPost**
> conversationsAgentOnlinePingPost(body)

Sets agent’s status to online for 2-3 minutes

We recommend pinging this endpoint every minute for as long as the agent has to be considered online.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ConversationsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ConversationsApi apiInstance = new ConversationsApi();
Body19 body = new Body19(); // Body19 | Agent fields.
try {
    apiInstance.conversationsAgentOnlinePingPost(body);
} catch (ApiException e) {
    System.err.println("Exception when calling ConversationsApi#conversationsAgentOnlinePingPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Body19**](Body19.md)| Agent fields. |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="conversationsMessagesIdDelete"></a>
# **conversationsMessagesIdDelete**
> conversationsMessagesIdDelete(id)

Delete a message sent by an agent

Only agents’ messages can be deleted.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ConversationsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ConversationsApi apiInstance = new ConversationsApi();
String id = "id_example"; // String | ID of the message
try {
    apiInstance.conversationsMessagesIdDelete(id);
} catch (ApiException e) {
    System.err.println("Exception when calling ConversationsApi#conversationsMessagesIdDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| ID of the message |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="conversationsMessagesIdGet"></a>
# **conversationsMessagesIdGet**
> ConversationsMessage conversationsMessagesIdGet(id)

Get a message

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ConversationsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ConversationsApi apiInstance = new ConversationsApi();
String id = "id_example"; // String | ID of the message
try {
    ConversationsMessage result = apiInstance.conversationsMessagesIdGet(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ConversationsApi#conversationsMessagesIdGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| ID of the message |

### Return type

[**ConversationsMessage**](ConversationsMessage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="conversationsMessagesIdPut"></a>
# **conversationsMessagesIdPut**
> ConversationsMessage conversationsMessagesIdPut(id, body)

Update a message sent by an agent

Only agents’ messages can be edited.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ConversationsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ConversationsApi apiInstance = new ConversationsApi();
String id = "id_example"; // String | ID of the message
Body16 body = new Body16(); // Body16 | 
try {
    ConversationsMessage result = apiInstance.conversationsMessagesIdPut(id, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ConversationsApi#conversationsMessagesIdPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| ID of the message |
 **body** | [**Body16**](Body16.md)|  | [optional]

### Return type

[**ConversationsMessage**](ConversationsMessage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="conversationsMessagesPost"></a>
# **conversationsMessagesPost**
> ConversationsMessage conversationsMessagesPost(body)

Send a message as an agent

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ConversationsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ConversationsApi apiInstance = new ConversationsApi();
Body15 body = new Body15(); // Body15 | Message fields.
try {
    ConversationsMessage result = apiInstance.conversationsMessagesPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ConversationsApi#conversationsMessagesPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Body15**](Body15.md)| Message fields. |

### Return type

[**ConversationsMessage**](ConversationsMessage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="conversationsPushedMessagesIdDelete"></a>
# **conversationsPushedMessagesIdDelete**
> conversationsPushedMessagesIdDelete(id)

Delete an automated message

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ConversationsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ConversationsApi apiInstance = new ConversationsApi();
String id = "id_example"; // String | ID of the message
try {
    apiInstance.conversationsPushedMessagesIdDelete(id);
} catch (ApiException e) {
    System.err.println("Exception when calling ConversationsApi#conversationsPushedMessagesIdDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| ID of the message |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="conversationsPushedMessagesIdGet"></a>
# **conversationsPushedMessagesIdGet**
> ConversationsMessage conversationsPushedMessagesIdGet(id)

Get an automated message

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ConversationsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ConversationsApi apiInstance = new ConversationsApi();
String id = "id_example"; // String | ID of the message sent previously
try {
    ConversationsMessage result = apiInstance.conversationsPushedMessagesIdGet(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ConversationsApi#conversationsPushedMessagesIdGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| ID of the message sent previously |

### Return type

[**ConversationsMessage**](ConversationsMessage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="conversationsPushedMessagesIdPut"></a>
# **conversationsPushedMessagesIdPut**
> ConversationsMessage conversationsPushedMessagesIdPut(id, body)

Update an automated message

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ConversationsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ConversationsApi apiInstance = new ConversationsApi();
String id = "id_example"; // String | ID of the message
Body18 body = new Body18(); // Body18 | 
try {
    ConversationsMessage result = apiInstance.conversationsPushedMessagesIdPut(id, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ConversationsApi#conversationsPushedMessagesIdPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| ID of the message |
 **body** | [**Body18**](Body18.md)|  |

### Return type

[**ConversationsMessage**](ConversationsMessage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="conversationsPushedMessagesPost"></a>
# **conversationsPushedMessagesPost**
> ConversationsMessage conversationsPushedMessagesPost(body)

Send an automated message to a visitor

Example of automated messages: order status, announce new features in your web app, etc.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ConversationsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ConversationsApi apiInstance = new ConversationsApi();
Body17 body = new Body17(); // Body17 | 
try {
    ConversationsMessage result = apiInstance.conversationsPushedMessagesPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ConversationsApi#conversationsPushedMessagesPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Body17**](Body17.md)|  |

### Return type

[**ConversationsMessage**](ConversationsMessage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

