# TierApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addSubscriptionToTier**](TierApi.md#addSubscriptionToTier) | **POST** /loyalty/tier/programs/{pid}/contacts/{cid}/tiers/{tid} | Assign a tier
[**createTierForTierGroup**](TierApi.md#createTierForTierGroup) | **POST** /loyalty/tier/programs/{pid}/tier-groups/{gid}/tiers | Create a tier
[**createTierGroup**](TierApi.md#createTierGroup) | **POST** /loyalty/tier/programs/{pid}/tier-groups | Create a tier group
[**deleteTier**](TierApi.md#deleteTier) | **DELETE** /loyalty/tier/programs/{pid}/tiers/{tid} | Delete tier
[**deleteTierGroup**](TierApi.md#deleteTierGroup) | **DELETE** /loyalty/tier/programs/{pid}/tier-groups/{gid} | Delete tier group
[**getListOfTierGroups**](TierApi.md#getListOfTierGroups) | **GET** /loyalty/tier/programs/{pid}/tier-groups | List tier groups
[**getLoyaltyProgramTier**](TierApi.md#getLoyaltyProgramTier) | **GET** /loyalty/tier/programs/{pid}/tiers | List tiers
[**getTierGroup**](TierApi.md#getTierGroup) | **GET** /loyalty/tier/programs/{pid}/tier-groups/{gid} | Get tier group
[**updateTier**](TierApi.md#updateTier) | **PUT** /loyalty/tier/programs/{pid}/tiers/{tid} | Update tier
[**updateTierGroup**](TierApi.md#updateTierGroup) | **PUT** /loyalty/tier/programs/{pid}/tier-groups/{gid} | Update tier group


<a name="addSubscriptionToTier"></a>
# **addSubscriptionToTier**
> TierForContact addSubscriptionToTier(pid, cid, tid)

Assign a tier

Manually assigns a tier to a specific membership.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
UUID cid = new UUID(); // UUID | Contact ID
UUID tid = new UUID(); // UUID | Tier ID
try {
    TierForContact result = apiInstance.addSubscriptionToTier(pid, cid, tid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#addSubscriptionToTier");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **cid** | [**UUID**](.md)| Contact ID |
 **tid** | [**UUID**](.md)| Tier ID |

### Return type

[**TierForContact**](TierForContact.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createTierForTierGroup"></a>
# **createTierForTierGroup**
> Tier createTierForTierGroup(pid, gid, payload)

Create a tier

Creates a new tier in a loyalty program tier group. *(The changes will take effect with the next publication of the loyalty program)*

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
UUID gid = new UUID(); // UUID | Tier group ID
TierRequest payload = new TierRequest(); // TierRequest | 
try {
    Tier result = apiInstance.createTierForTierGroup(pid, gid, payload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#createTierForTierGroup");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **gid** | [**UUID**](.md)| Tier group ID |
 **payload** | [**TierRequest**](TierRequest.md)|  |

### Return type

[**Tier**](Tier.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createTierGroup"></a>
# **createTierGroup**
> TierGroup createTierGroup(pid, payload)

Create a tier group

Creates a new tier group in a loyalty program. *(The changes will take effect with the next publication of the loyalty program)*

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
CreateTierGroupRequest payload = new CreateTierGroupRequest(); // CreateTierGroupRequest | Tier group creation payload
try {
    TierGroup result = apiInstance.createTierGroup(pid, payload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#createTierGroup");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **payload** | [**CreateTierGroupRequest**](CreateTierGroupRequest.md)| Tier group creation payload |

### Return type

[**TierGroup**](TierGroup.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteTier"></a>
# **deleteTier**
> String deleteTier(pid, tid)

Delete tier

Deletes a tier from a loyalty program tier group. *(The changes will take effect with the next publication of the loyalty program)*

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
UUID tid = new UUID(); // UUID | Tier ID
try {
    String result = apiInstance.deleteTier(pid, tid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#deleteTier");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **tid** | [**UUID**](.md)| Tier ID |

### Return type

**String**

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteTierGroup"></a>
# **deleteTierGroup**
> String deleteTierGroup(pid, gid)

Delete tier group

Deletes a tier group from a loyalty program. *(The changes will take effect with the next publication of the loyalty program)*

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
UUID gid = new UUID(); // UUID | Tier group ID
try {
    String result = apiInstance.deleteTierGroup(pid, gid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#deleteTierGroup");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **gid** | [**UUID**](.md)| Tier group ID |

### Return type

**String**

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getListOfTierGroups"></a>
# **getListOfTierGroups**
> TierGroupPage getListOfTierGroups(pid, version)

List tier groups

Returns the list of tier groups defined within the loyalty program.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
String version = "draft"; // String | Select 'active' to retrieve list of all tier groups which are live for clients. Select draft to retrieve list of all non deleted tier groups.
try {
    TierGroupPage result = apiInstance.getListOfTierGroups(pid, version);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#getListOfTierGroups");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **version** | **String**| Select &#39;active&#39; to retrieve list of all tier groups which are live for clients. Select draft to retrieve list of all non deleted tier groups. | [optional] [default to draft] [enum: active, draft]

### Return type

[**TierGroupPage**](TierGroupPage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getLoyaltyProgramTier"></a>
# **getLoyaltyProgramTier**
> LoyaltyTierPage getLoyaltyProgramTier(pid, version)

List tiers

Returns the list of tiers defined within the loyalty program.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
String version = "draft"; // String | Select 'active' to retrieve list of all tiers which are live for clients. Select draft to retrieve list of all non deleted tiers.
try {
    LoyaltyTierPage result = apiInstance.getLoyaltyProgramTier(pid, version);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#getLoyaltyProgramTier");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **version** | **String**| Select &#39;active&#39; to retrieve list of all tiers which are live for clients. Select draft to retrieve list of all non deleted tiers. | [optional] [default to draft] [enum: active, draft]

### Return type

[**LoyaltyTierPage**](LoyaltyTierPage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getTierGroup"></a>
# **getTierGroup**
> TierGroup getTierGroup(pid, gid, version)

Get tier group

Returns tier group information.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
UUID gid = new UUID(); // UUID | Tier group ID
String version = "draft"; // String | Select active to retrieve active version of tier group. Select draft to retrieve latest changes in tier group.
try {
    TierGroup result = apiInstance.getTierGroup(pid, gid, version);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#getTierGroup");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **gid** | [**UUID**](.md)| Tier group ID |
 **version** | **String**| Select active to retrieve active version of tier group. Select draft to retrieve latest changes in tier group. | [optional] [default to draft] [enum: active, draft]

### Return type

[**TierGroup**](TierGroup.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateTier"></a>
# **updateTier**
> Tier updateTier(pid, tid, payload)

Update tier

Modifies an existing tier for the specified tier group *(The changes will take effect with the next publication of the loyalty program)*

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
UUID tid = new UUID(); // UUID | Tier ID
TierRequestPutPayload payload = new TierRequestPutPayload(); // TierRequestPutPayload | 
try {
    Tier result = apiInstance.updateTier(pid, tid, payload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#updateTier");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **tid** | [**UUID**](.md)| Tier ID |
 **payload** | [**TierRequestPutPayload**](TierRequestPutPayload.md)|  |

### Return type

[**Tier**](Tier.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateTierGroup"></a>
# **updateTierGroup**
> TierGroup updateTierGroup(pid, gid, payload)

Update tier group

Updates a tier group from a loyalty program. *(The changes will take effect with the next publication of the loyalty program)*

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TierApi;

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

TierApi apiInstance = new TierApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
UUID gid = new UUID(); // UUID | Tier group ID
UpdateTierGroupRequest payload = new UpdateTierGroupRequest(); // UpdateTierGroupRequest | Tier group update payload
try {
    TierGroup result = apiInstance.updateTierGroup(pid, gid, payload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TierApi#updateTierGroup");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **gid** | [**UUID**](.md)| Tier group ID |
 **payload** | [**UpdateTierGroupRequest**](UpdateTierGroupRequest.md)| Tier group update payload |

### Return type

[**TierGroup**](TierGroup.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

