# ProgramApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewLP**](ProgramApi.md#createNewLP) | **POST** /loyalty/config/programs | Create loyalty program
[**deleteContactMembers**](ProgramApi.md#deleteContactMembers) | **DELETE** /loyalty/config/programs/{pid}/subscription-members | Delete subscription member
[**deleteLoyaltyProgram**](ProgramApi.md#deleteLoyaltyProgram) | **DELETE** /loyalty/config/programs/{pid} | Delete Loyalty Program
[**getLPList**](ProgramApi.md#getLPList) | **GET** /loyalty/config/programs | Get loyalty program list
[**getLoyaltyProgramInfo**](ProgramApi.md#getLoyaltyProgramInfo) | **GET** /loyalty/config/programs/{pid} | Get loyalty program Info
[**getParameterSubscriptionInfo**](ProgramApi.md#getParameterSubscriptionInfo) | **GET** /loyalty/config/programs/{pid}/account-info | Get Subscription Data
[**loyaltyConfigProgramsPidContactCidDelete**](ProgramApi.md#loyaltyConfigProgramsPidContactCidDelete) | **DELETE** /loyalty/config/programs/{pid}/contact/{cid} | Delete subscription
[**partiallyUpdateLoyaltyProgram**](ProgramApi.md#partiallyUpdateLoyaltyProgram) | **PATCH** /loyalty/config/programs/{pid} | Partially update loyalty program
[**publishLoyaltyProgram**](ProgramApi.md#publishLoyaltyProgram) | **POST** /loyalty/config/programs/{pid}/publish | Publish loyalty program
[**subscribeMemberToASubscription**](ProgramApi.md#subscribeMemberToASubscription) | **POST** /loyalty/config/programs/{pid}/subscription-members | Create subscription member
[**subscribeToLoyaltyProgram**](ProgramApi.md#subscribeToLoyaltyProgram) | **POST** /loyalty/config/programs/{pid}/subscriptions | Create subscription
[**updateLoyaltyProgram**](ProgramApi.md#updateLoyaltyProgram) | **PUT** /loyalty/config/programs/{pid} | Update loyalty program


<a name="createNewLP"></a>
# **createNewLP**
> LoyaltyProgram createNewLP(body)

Create loyalty program

Creates loyalty program

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.ProgramApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api-key.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

ProgramApi apiInstance = new ProgramApi();
CreateLoyaltyProgramPayload body = new CreateLoyaltyProgramPayload(); // CreateLoyaltyProgramPayload | Create Loyalty Program Payload
try {
    LoyaltyProgram result = apiInstance.createNewLP(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#createNewLP");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CreateLoyaltyProgramPayload**](CreateLoyaltyProgramPayload.md)| Create Loyalty Program Payload |

### Return type

[**LoyaltyProgram**](LoyaltyProgram.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteContactMembers"></a>
# **deleteContactMembers**
> deleteContactMembers(pid, memberContactIds)

Delete subscription member

Deletes member from a subscription

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
String memberContactIds = "memberContactIds_example"; // String | Member Contact Ids
try {
    apiInstance.deleteContactMembers(pid, memberContactIds);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#deleteContactMembers");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **memberContactIds** | **String**| Member Contact Ids |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteLoyaltyProgram"></a>
# **deleteLoyaltyProgram**
> deleteLoyaltyProgram(pid)

Delete Loyalty Program

Deletes Loyalty Program

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
try {
    apiInstance.deleteLoyaltyProgram(pid);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#deleteLoyaltyProgram");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getLPList"></a>
# **getLPList**
> LoyaltyProgramPage getLPList(limit, offset, sortField, sort)

Get loyalty program list

Returns list of loyalty programs

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
Integer limit = 56; // Integer | Number of documents per page
Integer offset = 56; // Integer | Index of the first document in the page
String sortField = "sortField_example"; // String | Sort documents by field
String sort = "sort_example"; // String | Sort the documents in the ascending or descending order
try {
    LoyaltyProgramPage result = apiInstance.getLPList(limit, offset, sortField, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#getLPList");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Integer**| Number of documents per page | [optional]
 **offset** | **Integer**| Index of the first document in the page | [optional]
 **sortField** | **String**| Sort documents by field | [optional] [enum: name, created_at, updated_at]
 **sort** | **String**| Sort the documents in the ascending or descending order | [optional]

### Return type

[**LoyaltyProgramPage**](LoyaltyProgramPage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getLoyaltyProgramInfo"></a>
# **getLoyaltyProgramInfo**
> LoyaltyProgram getLoyaltyProgramInfo(pid)

Get loyalty program Info

Returns loyalty program

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
try {
    LoyaltyProgram result = apiInstance.getLoyaltyProgramInfo(pid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#getLoyaltyProgramInfo");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |

### Return type

[**LoyaltyProgram**](LoyaltyProgram.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getParameterSubscriptionInfo"></a>
# **getParameterSubscriptionInfo**
> SubscriptionHandlerInfo getParameterSubscriptionInfo(pid, contactId, params, loyaltySubscriptionId, includeInternal)

Get Subscription Data

Get Information of balances, tiers, rewards and subscription members for a subscription

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
String contactId = "contactId_example"; // String | Contact Id
String params = "params_example"; // String | Filter List
String loyaltySubscriptionId = "loyaltySubscriptionId_example"; // String | Loyalty Subscription Id
Boolean includeInternal = true; // Boolean | Include Internal
try {
    SubscriptionHandlerInfo result = apiInstance.getParameterSubscriptionInfo(pid, contactId, params, loyaltySubscriptionId, includeInternal);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#getParameterSubscriptionInfo");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **contactId** | **String**| Contact Id | [optional]
 **params** | **String**| Filter List | [optional]
 **loyaltySubscriptionId** | **String**| Loyalty Subscription Id | [optional]
 **includeInternal** | **Boolean**| Include Internal | [optional]

### Return type

[**SubscriptionHandlerInfo**](SubscriptionHandlerInfo.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyConfigProgramsPidContactCidDelete"></a>
# **loyaltyConfigProgramsPidContactCidDelete**
> TransactionHistoryResp loyaltyConfigProgramsPidContactCidDelete(pid, cid)

Delete subscription

Delete subscription for a contact

### Example
```java
// Import classes:
//import io.swagger.client.ApiClient;
//import io.swagger.client.ApiException;
//import io.swagger.client.Configuration;
//import io.swagger.client.auth.*;
//import io.swagger.client.api.ProgramApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api-key.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partner-key.setApiKeyPrefix("Token");

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID. A unique identifier for the loyalty program.
Integer cid = 56; // Integer | Contact ID.
try {
    TransactionHistoryResp result = apiInstance.loyaltyConfigProgramsPidContactCidDelete(pid, cid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#loyaltyConfigProgramsPidContactCidDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID. A unique identifier for the loyalty program. |
 **cid** | **Integer**| Contact ID. |

### Return type

[**TransactionHistoryResp**](TransactionHistoryResp.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="partiallyUpdateLoyaltyProgram"></a>
# **partiallyUpdateLoyaltyProgram**
> LoyaltyProgram partiallyUpdateLoyaltyProgram(pid, body)

Partially update loyalty program

Partially updates loyalty program

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
PatchLoyaltyProgramPayload body = new PatchLoyaltyProgramPayload(); // PatchLoyaltyProgramPayload | Loyalty Program Payload
try {
    LoyaltyProgram result = apiInstance.partiallyUpdateLoyaltyProgram(pid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#partiallyUpdateLoyaltyProgram");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **body** | [**PatchLoyaltyProgramPayload**](PatchLoyaltyProgramPayload.md)| Loyalty Program Payload |

### Return type

[**LoyaltyProgram**](LoyaltyProgram.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="publishLoyaltyProgram"></a>
# **publishLoyaltyProgram**
> publishLoyaltyProgram(pid)

Publish loyalty program

Publishes loyalty program

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
try {
    apiInstance.publishLoyaltyProgram(pid);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#publishLoyaltyProgram");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="subscribeMemberToASubscription"></a>
# **subscribeMemberToASubscription**
> SubscriptionMember subscribeMemberToASubscription(pid, body)

Create subscription member

Add member to a subscription

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
AddSubscriptionMemberPayload body = new AddSubscriptionMemberPayload(); // AddSubscriptionMemberPayload | Add Subscription Member Payload
try {
    SubscriptionMember result = apiInstance.subscribeMemberToASubscription(pid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#subscribeMemberToASubscription");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **body** | [**AddSubscriptionMemberPayload**](AddSubscriptionMemberPayload.md)| Add Subscription Member Payload |

### Return type

[**SubscriptionMember**](SubscriptionMember.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="subscribeToLoyaltyProgram"></a>
# **subscribeToLoyaltyProgram**
> Subscription subscribeToLoyaltyProgram(pid, body)

Create subscription

Subscribes to a loyalty program

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
CreateSubscriptionPayload body = new CreateSubscriptionPayload(); // CreateSubscriptionPayload | Create Subscription Payload
try {
    Subscription result = apiInstance.subscribeToLoyaltyProgram(pid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#subscribeToLoyaltyProgram");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **body** | [**CreateSubscriptionPayload**](CreateSubscriptionPayload.md)| Create Subscription Payload |

### Return type

[**Subscription**](Subscription.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateLoyaltyProgram"></a>
# **updateLoyaltyProgram**
> LoyaltyProgram updateLoyaltyProgram(pid, body)

Update loyalty program

Updates loyalty program

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ProgramApi;

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

ProgramApi apiInstance = new ProgramApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UpdateLoyaltyProgramPayload body = new UpdateLoyaltyProgramPayload(); // UpdateLoyaltyProgramPayload | Update Loyalty Program Payload
try {
    LoyaltyProgram result = apiInstance.updateLoyaltyProgram(pid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProgramApi#updateLoyaltyProgram");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **body** | [**UpdateLoyaltyProgramPayload**](UpdateLoyaltyProgramPayload.md)| Update Loyalty Program Payload |

### Return type

[**LoyaltyProgram**](LoyaltyProgram.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

