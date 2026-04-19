# BalanceApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**beginTransaction**](BalanceApi.md#beginTransaction) | **POST** /loyalty/balance/programs/{pid}/transactions | Create new transaction
[**cancelTransaction**](BalanceApi.md#cancelTransaction) | **POST** /loyalty/balance/programs/{pid}/transactions/{tid}/cancel | Cancel transaction
[**completeTransaction**](BalanceApi.md#completeTransaction) | **POST** /loyalty/balance/programs/{pid}/transactions/{tid}/complete | Complete transaction
[**createBalanceLimit**](BalanceApi.md#createBalanceLimit) | **POST** /loyalty/balance/programs/{pid}/balance-definitions/{bdid}/limits | Create balance limits
[**createBalanceOrder**](BalanceApi.md#createBalanceOrder) | **POST** /loyalty/balance/programs/{pid}/create-order | Create balance order
[**deleteBalanceDefinition**](BalanceApi.md#deleteBalanceDefinition) | **DELETE** /loyalty/balance/programs/{pid}/balance-definitions/{bdid} | Delete balance definition
[**deleteBalanceLimit**](BalanceApi.md#deleteBalanceLimit) | **DELETE** /loyalty/balance/programs/{pid}/balance-definitions/{bdid}/limits/{blid} | Delete balance limit
[**getBalanceDefinition**](BalanceApi.md#getBalanceDefinition) | **GET** /loyalty/balance/programs/{pid}/balance-definitions/{bdid} | Get balance definition
[**getBalanceDefinitionList**](BalanceApi.md#getBalanceDefinitionList) | **GET** /loyalty/balance/programs/{pid}/balance-definitions | Get balance definition list
[**getBalanceLimit**](BalanceApi.md#getBalanceLimit) | **GET** /loyalty/balance/programs/{pid}/balance-definitions/{bdid}/limits/{blid} | Get balance limits
[**getContactBalances**](BalanceApi.md#getContactBalances) | **GET** /loyalty/balance/programs/{pid}/contact-balances | Get balance list
[**getSubscriptionBalances**](BalanceApi.md#getSubscriptionBalances) | **GET** /loyalty/balance/programs/{pid}/subscriptions/{cid}/balances | Get subscription balances
[**loyaltyBalanceProgramsPidActiveBalanceGet**](BalanceApi.md#loyaltyBalanceProgramsPidActiveBalanceGet) | **GET** /loyalty/balance/programs/{pid}/active-balance | Get Active Balances API
[**loyaltyBalanceProgramsPidBalanceDefinitionsPost**](BalanceApi.md#loyaltyBalanceProgramsPidBalanceDefinitionsPost) | **POST** /loyalty/balance/programs/{pid}/balance-definitions | Create balance definition
[**loyaltyBalanceProgramsPidSubscriptionsCidBalancesPost**](BalanceApi.md#loyaltyBalanceProgramsPidSubscriptionsCidBalancesPost) | **POST** /loyalty/balance/programs/{pid}/subscriptions/{cid}/balances | Create subscription balances
[**loyaltyBalanceProgramsPidTransactionHistoryGet**](BalanceApi.md#loyaltyBalanceProgramsPidTransactionHistoryGet) | **GET** /loyalty/balance/programs/{pid}/transaction-history | Get Transaction History API
[**updateBalanceDefinition**](BalanceApi.md#updateBalanceDefinition) | **PUT** /loyalty/balance/programs/{pid}/balance-definitions/{bdid} | Update balance definition
[**updateBalanceLimit**](BalanceApi.md#updateBalanceLimit) | **PUT** /loyalty/balance/programs/{pid}/balance-definitions/{bdid}/limits/{blid} | Updates balance limit


<a name="beginTransaction"></a>
# **beginTransaction**
> Transaction beginTransaction(pid, body)

Create new transaction

Creates new transaction and returns information

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
CreateTransactionPayload body = new CreateTransactionPayload(); // CreateTransactionPayload | Transaction Payload
try {
    Transaction result = apiInstance.beginTransaction(pid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#beginTransaction");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **body** | [**CreateTransactionPayload**](CreateTransactionPayload.md)| Transaction Payload |

### Return type

[**Transaction**](Transaction.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="cancelTransaction"></a>
# **cancelTransaction**
> Transaction cancelTransaction(pid, tid)

Cancel transaction

Cancels transaction

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UUID tid = new UUID(); // UUID | Transaction Id
try {
    Transaction result = apiInstance.cancelTransaction(pid, tid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#cancelTransaction");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **tid** | [**UUID**](.md)| Transaction Id |

### Return type

[**Transaction**](Transaction.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="completeTransaction"></a>
# **completeTransaction**
> Transaction completeTransaction(pid, tid)

Complete transaction

Completes transaction

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UUID tid = new UUID(); // UUID | Transaction Id
try {
    Transaction result = apiInstance.completeTransaction(pid, tid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#completeTransaction");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **tid** | [**UUID**](.md)| Transaction Id |

### Return type

[**Transaction**](Transaction.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createBalanceLimit"></a>
# **createBalanceLimit**
> BalanceLimit createBalanceLimit(pid, bdid, body)

Create balance limits

Creates balance limit and sends the created UUID along with the data

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UUID bdid = new UUID(); // UUID | Balance Definition Id
CreateBalanceLimitPayload body = new CreateBalanceLimitPayload(); // CreateBalanceLimitPayload | Balance Definition Payload
try {
    BalanceLimit result = apiInstance.createBalanceLimit(pid, bdid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#createBalanceLimit");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **bdid** | [**UUID**](.md)| Balance Definition Id |
 **body** | [**CreateBalanceLimitPayload**](CreateBalanceLimitPayload.md)| Balance Definition Payload |

### Return type

[**BalanceLimit**](BalanceLimit.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createBalanceOrder"></a>
# **createBalanceOrder**
> BalanceOrder createBalanceOrder(pid, body)

Create balance order

Returns created order

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
CreateOrderPayload body = new CreateOrderPayload(); // CreateOrderPayload | Order Payload
try {
    BalanceOrder result = apiInstance.createBalanceOrder(pid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#createBalanceOrder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **body** | [**CreateOrderPayload**](CreateOrderPayload.md)| Order Payload |

### Return type

[**BalanceOrder**](BalanceOrder.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteBalanceDefinition"></a>
# **deleteBalanceDefinition**
> deleteBalanceDefinition(pid, bdid)

Delete balance definition

Delete Balance definition

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UUID bdid = new UUID(); // UUID | Balance Definition Id
try {
    apiInstance.deleteBalanceDefinition(pid, bdid);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#deleteBalanceDefinition");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **bdid** | [**UUID**](.md)| Balance Definition Id |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteBalanceLimit"></a>
# **deleteBalanceLimit**
> deleteBalanceLimit(pid, bdid, blid)

Delete balance limit

Delete balance limit

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UUID bdid = new UUID(); // UUID | Balance Definition Id
UUID blid = new UUID(); // UUID | Balance Limit Id
try {
    apiInstance.deleteBalanceLimit(pid, bdid, blid);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#deleteBalanceLimit");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **bdid** | [**UUID**](.md)| Balance Definition Id |
 **blid** | [**UUID**](.md)| Balance Limit Id |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getBalanceDefinition"></a>
# **getBalanceDefinition**
> BalanceDefinition getBalanceDefinition(pid, bdid, version)

Get balance definition

Returns balance definition

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UUID bdid = new UUID(); // UUID | Balance Definition Id
String version = "draft"; // String | Version
try {
    BalanceDefinition result = apiInstance.getBalanceDefinition(pid, bdid, version);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#getBalanceDefinition");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **bdid** | [**UUID**](.md)| Balance Definition Id |
 **version** | **String**| Version | [optional] [default to draft] [enum: active, draft]

### Return type

[**BalanceDefinition**](BalanceDefinition.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getBalanceDefinitionList"></a>
# **getBalanceDefinitionList**
> BalanceDefinitionPage getBalanceDefinitionList(pid, limit, offset, sortField, sort, version)

Get balance definition list

Returns balance definition page

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
Integer limit = 200; // Integer | Limit the number of records returned
Integer offset = 0; // Integer | Offset to paginate records
String sortField = "updated_at"; // String | Field to sort by
String sort = "desc"; // String | Sort direction
String version = "draft"; // String | Version
try {
    BalanceDefinitionPage result = apiInstance.getBalanceDefinitionList(pid, limit, offset, sortField, sort, version);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#getBalanceDefinitionList");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **limit** | **Integer**| Limit the number of records returned | [optional] [default to 200]
 **offset** | **Integer**| Offset to paginate records | [optional] [default to 0]
 **sortField** | **String**| Field to sort by | [optional] [default to updated_at] [enum: name, created_at, updated_at]
 **sort** | **String**| Sort direction | [optional] [default to desc] [enum: asc, desc]
 **version** | **String**| Version | [optional] [default to draft] [enum: active, draft]

### Return type

[**BalanceDefinitionPage**](BalanceDefinitionPage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getBalanceLimit"></a>
# **getBalanceLimit**
> BalanceLimit getBalanceLimit(pid, bdid, blid, version)

Get balance limits

Fetches balance limits and send the created UUID along with the data

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UUID bdid = new UUID(); // UUID | Balance Definition Id
UUID blid = new UUID(); // UUID | Balance Limit Id
String version = "draft"; // String | Version
try {
    BalanceLimit result = apiInstance.getBalanceLimit(pid, bdid, blid, version);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#getBalanceLimit");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **bdid** | [**UUID**](.md)| Balance Definition Id |
 **blid** | [**UUID**](.md)| Balance Limit Id |
 **version** | **String**| Version | [optional] [default to draft] [enum: active, draft]

### Return type

[**BalanceLimit**](BalanceLimit.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getContactBalances"></a>
# **getContactBalances**
> ContactBalancesResp getContactBalances(pid, includeInternal)

Get balance list

Returns balance list

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
Boolean includeInternal = true; // Boolean | Include Internal
try {
    ContactBalancesResp result = apiInstance.getContactBalances(pid, includeInternal);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#getContactBalances");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **includeInternal** | **Boolean**| Include Internal | [optional]

### Return type

[**ContactBalancesResp**](ContactBalancesResp.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getSubscriptionBalances"></a>
# **getSubscriptionBalances**
> ModelSubscriptionBalanceResp getSubscriptionBalances(cid, pid, includeInternal)

Get subscription balances

Returns subscription balances

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
String cid = "cid_example"; // String | Contact Id
UUID pid = new UUID(); // UUID | Loyalty Program Id
Boolean includeInternal = true; // Boolean | Include Internal
try {
    ModelSubscriptionBalanceResp result = apiInstance.getSubscriptionBalances(cid, pid, includeInternal);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#getSubscriptionBalances");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cid** | **String**| Contact Id |
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **includeInternal** | **Boolean**| Include Internal | [optional]

### Return type

[**ModelSubscriptionBalanceResp**](ModelSubscriptionBalanceResp.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyBalanceProgramsPidActiveBalanceGet"></a>
# **loyaltyBalanceProgramsPidActiveBalanceGet**
> BalanceLimit loyaltyBalanceProgramsPidActiveBalanceGet(pid, contactId, balanceDefinitionId, limit, offset, sortField, sort, includeInternal)

Get Active Balances API

Returns Active Balances

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
Integer contactId = 56; // Integer | Contact ID
UUID balanceDefinitionId = new UUID(); // UUID | Balance Definition ID
Integer limit = 56; // Integer | Limit
Integer offset = 56; // Integer | Offset
String sortField = "sortField_example"; // String | Sort Field
String sort = "sort_example"; // String | Sort Order
Boolean includeInternal = true; // Boolean | Include Internal
try {
    BalanceLimit result = apiInstance.loyaltyBalanceProgramsPidActiveBalanceGet(pid, contactId, balanceDefinitionId, limit, offset, sortField, sort, includeInternal);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#loyaltyBalanceProgramsPidActiveBalanceGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **contactId** | **Integer**| Contact ID |
 **balanceDefinitionId** | [**UUID**](.md)| Balance Definition ID |
 **limit** | **Integer**| Limit | [optional]
 **offset** | **Integer**| Offset | [optional]
 **sortField** | **String**| Sort Field | [optional]
 **sort** | **String**| Sort Order | [optional]
 **includeInternal** | **Boolean**| Include Internal | [optional]

### Return type

[**BalanceLimit**](BalanceLimit.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyBalanceProgramsPidBalanceDefinitionsPost"></a>
# **loyaltyBalanceProgramsPidBalanceDefinitionsPost**
> BalanceDefinition loyaltyBalanceProgramsPidBalanceDefinitionsPost(pid, body)

Create balance definition

Creates balance definition and returns information

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
CreateBalanceDefinitionPayload body = new CreateBalanceDefinitionPayload(); // CreateBalanceDefinitionPayload | Create Balance Definition Payload
try {
    BalanceDefinition result = apiInstance.loyaltyBalanceProgramsPidBalanceDefinitionsPost(pid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#loyaltyBalanceProgramsPidBalanceDefinitionsPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **body** | [**CreateBalanceDefinitionPayload**](CreateBalanceDefinitionPayload.md)| Create Balance Definition Payload |

### Return type

[**BalanceDefinition**](BalanceDefinition.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyBalanceProgramsPidSubscriptionsCidBalancesPost"></a>
# **loyaltyBalanceProgramsPidSubscriptionsCidBalancesPost**
> Balance loyaltyBalanceProgramsPidSubscriptionsCidBalancesPost(pid, cid, body)

Create subscription balances

Creates a balance for a contact

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
String cid = "cid_example"; // String | Contact Id
CreateBalancePayload body = new CreateBalancePayload(); // CreateBalancePayload | Create Balnce Payload
try {
    Balance result = apiInstance.loyaltyBalanceProgramsPidSubscriptionsCidBalancesPost(pid, cid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#loyaltyBalanceProgramsPidSubscriptionsCidBalancesPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **cid** | **String**| Contact Id |
 **body** | [**CreateBalancePayload**](CreateBalancePayload.md)| Create Balnce Payload |

### Return type

[**Balance**](Balance.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyBalanceProgramsPidTransactionHistoryGet"></a>
# **loyaltyBalanceProgramsPidTransactionHistoryGet**
> TransactionHistoryResp loyaltyBalanceProgramsPidTransactionHistoryGet(pid, contactId, balanceDefinitionId, limit, offset, sortField, sort, filters, metadata, status, transactionType, loyaltySubscriptionId)

Get Transaction History API

Returns transaction history

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
Integer contactId = 0; // Integer | Contact ID
UUID balanceDefinitionId = new UUID(); // UUID | Balance Definition ID
Integer limit = 20; // Integer | Limit the number of records returned
Integer offset = 0; // Integer | Skip a number of records
String sortField = "createdAt"; // String | Field to sort by
String sort = "desc"; // String | Sort order, either asc or desc
List<String> filters = Arrays.asList("filters_example"); // List<String> | Filters to apply
Map<String, String> metadata = new HashMap<String, String>(); // Map<String, String> | Filter transactions by metadata key-value pairs
String status = "status_example"; // String | Filter by transaction status
String transactionType = "transactionType_example"; // String | Filter by transaction type
String loyaltySubscriptionId = "loyaltySubscriptionId_example"; // String | Loyalty Subscription ID filter
try {
    TransactionHistoryResp result = apiInstance.loyaltyBalanceProgramsPidTransactionHistoryGet(pid, contactId, balanceDefinitionId, limit, offset, sortField, sort, filters, metadata, status, transactionType, loyaltySubscriptionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#loyaltyBalanceProgramsPidTransactionHistoryGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **contactId** | **Integer**| Contact ID | [default to 0]
 **balanceDefinitionId** | [**UUID**](.md)| Balance Definition ID |
 **limit** | **Integer**| Limit the number of records returned | [optional] [default to 20]
 **offset** | **Integer**| Skip a number of records | [optional] [default to 0]
 **sortField** | **String**| Field to sort by | [optional] [default to createdAt] [enum: createdAt]
 **sort** | **String**| Sort order, either asc or desc | [optional] [default to desc] [enum: asc, desc]
 **filters** | [**List&lt;String&gt;**](String.md)| Filters to apply | [optional]
 **metadata** | [**Map&lt;String, String&gt;**](String.md)| Filter transactions by metadata key-value pairs | [optional]
 **status** | **String**| Filter by transaction status | [optional]
 **transactionType** | **String**| Filter by transaction type | [optional]
 **loyaltySubscriptionId** | **String**| Loyalty Subscription ID filter | [optional]

### Return type

[**TransactionHistoryResp**](TransactionHistoryResp.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateBalanceDefinition"></a>
# **updateBalanceDefinition**
> BalanceDefinition updateBalanceDefinition(pid, bdid, body)

Update balance definition

Updates Balance definition

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UUID bdid = new UUID(); // UUID | Balance Definition Id
UpdateBalanceDefinitionPayload body = new UpdateBalanceDefinitionPayload(); // UpdateBalanceDefinitionPayload | Update Balance Definition Payload
try {
    BalanceDefinition result = apiInstance.updateBalanceDefinition(pid, bdid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#updateBalanceDefinition");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **bdid** | [**UUID**](.md)| Balance Definition Id |
 **body** | [**UpdateBalanceDefinitionPayload**](UpdateBalanceDefinitionPayload.md)| Update Balance Definition Payload |

### Return type

[**BalanceDefinition**](BalanceDefinition.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateBalanceLimit"></a>
# **updateBalanceLimit**
> BalanceLimit updateBalanceLimit(pid, bdid, blid, body)

Updates balance limit

Updates balance limit

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.BalanceApi;

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

BalanceApi apiInstance = new BalanceApi();
UUID pid = new UUID(); // UUID | Loyalty Program Id
UUID bdid = new UUID(); // UUID | Balance Definition Id
UUID blid = new UUID(); // UUID | Balance Limit Id
UpdateBalanceLimitPayload body = new UpdateBalanceLimitPayload(); // UpdateBalanceLimitPayload | Balance Limits Payload
try {
    BalanceLimit result = apiInstance.updateBalanceLimit(pid, bdid, blid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling BalanceApi#updateBalanceLimit");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program Id |
 **bdid** | [**UUID**](.md)| Balance Definition Id |
 **blid** | [**UUID**](.md)| Balance Limit Id |
 **body** | [**UpdateBalanceLimitPayload**](UpdateBalanceLimitPayload.md)| Balance Limits Payload |

### Return type

[**BalanceLimit**](BalanceLimit.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

