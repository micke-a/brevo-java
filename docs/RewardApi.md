# RewardApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCodeCount**](RewardApi.md#getCodeCount) | **GET** /loyalty/offer/programs/{pid}/code-pools/{cpid}/codes-count | Get code count
[**loyaltyOfferProgramsPidOffersGet**](RewardApi.md#loyaltyOfferProgramsPidOffersGet) | **GET** /loyalty/offer/programs/{pid}/offers | Get Reward Page API
[**loyaltyOfferProgramsPidOffersPost**](RewardApi.md#loyaltyOfferProgramsPidOffersPost) | **POST** /loyalty/offer/programs/{pid}/offers | Create a reward
[**loyaltyOfferProgramsPidRewardsAttributePost**](RewardApi.md#loyaltyOfferProgramsPidRewardsAttributePost) | **POST** /loyalty/offer/programs/{pid}/rewards/attribute | Create a voucher
[**loyaltyOfferProgramsPidRewardsRedeemPost**](RewardApi.md#loyaltyOfferProgramsPidRewardsRedeemPost) | **POST** /loyalty/offer/programs/{pid}/rewards/redeem | Create redeem voucher request
[**loyaltyOfferProgramsPidRewardsRedeemTidCompletePost**](RewardApi.md#loyaltyOfferProgramsPidRewardsRedeemTidCompletePost) | **POST** /loyalty/offer/programs/{pid}/rewards/redeem/{tid}/complete | Complete redeem voucher request
[**loyaltyOfferProgramsPidRewardsRevokeDelete**](RewardApi.md#loyaltyOfferProgramsPidRewardsRevokeDelete) | **DELETE** /loyalty/offer/programs/{pid}/rewards/revoke | Revoke vouchers
[**loyaltyOfferProgramsPidRewardsRidGet**](RewardApi.md#loyaltyOfferProgramsPidRewardsRidGet) | **GET** /loyalty/offer/programs/{pid}/rewards/{rid} | Get reward information
[**loyaltyOfferProgramsPidRewardsValidatePost**](RewardApi.md#loyaltyOfferProgramsPidRewardsValidatePost) | **POST** /loyalty/offer/programs/{pid}/rewards/validate | Validate a reward
[**loyaltyOfferProgramsPidVouchersGet**](RewardApi.md#loyaltyOfferProgramsPidVouchersGet) | **GET** /loyalty/offer/programs/{pid}/vouchers | Get voucher for a contact


<a name="getCodeCount"></a>
# **getCodeCount**
> MainCodeCountHttpResponse getCodeCount(pid, cpid)

Get code count

Get code count

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
UUID cpid = new UUID(); // UUID | Code Pool ID
try {
    MainCodeCountHttpResponse result = apiInstance.getCodeCount(pid, cpid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#getCodeCount");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **cpid** | [**UUID**](.md)| Code Pool ID |

### Return type

[**MainCodeCountHttpResponse**](MainCodeCountHttpResponse.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyOfferProgramsPidOffersGet"></a>
# **loyaltyOfferProgramsPidOffersGet**
> MainRewardPage loyaltyOfferProgramsPidOffersGet(pid, limit, offset, state, version)

Get Reward Page API

Returns a reward page

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
Integer limit = 25; // Integer | Page size
Integer offset = 0; // Integer | Pagination offset
String state = "all"; // String | State of the reward
String version = "draft"; // String | Version
try {
    MainRewardPage result = apiInstance.loyaltyOfferProgramsPidOffersGet(pid, limit, offset, state, version);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#loyaltyOfferProgramsPidOffersGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **limit** | **Integer**| Page size | [optional] [default to 25]
 **offset** | **Integer**| Pagination offset | [optional] [default to 0]
 **state** | **String**| State of the reward | [optional] [default to all]
 **version** | **String**| Version | [optional] [default to draft] [enum: active, draft]

### Return type

[**MainRewardPage**](MainRewardPage.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyOfferProgramsPidOffersPost"></a>
# **loyaltyOfferProgramsPidOffersPost**
> MainCreateRewardResponse loyaltyOfferProgramsPidOffersPost(pid, payload)

Create a reward

Creates a new reward in loyalty program.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
MainCreateRewardPayload payload = new MainCreateRewardPayload(); // MainCreateRewardPayload | Reward creation payload
try {
    MainCreateRewardResponse result = apiInstance.loyaltyOfferProgramsPidOffersPost(pid, payload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#loyaltyOfferProgramsPidOffersPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **payload** | [**MainCreateRewardPayload**](MainCreateRewardPayload.md)| Reward creation payload |

### Return type

[**MainCreateRewardResponse**](MainCreateRewardResponse.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyOfferProgramsPidRewardsAttributePost"></a>
# **loyaltyOfferProgramsPidRewardsAttributePost**
> MainRewardAttribution loyaltyOfferProgramsPidRewardsAttributePost(pid, payload)

Create a voucher

Create a voucher and attribute it to a specific membership.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
MainAttributeRewardPayload payload = new MainAttributeRewardPayload(); // MainAttributeRewardPayload | Voucher creation payload
try {
    MainRewardAttribution result = apiInstance.loyaltyOfferProgramsPidRewardsAttributePost(pid, payload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#loyaltyOfferProgramsPidRewardsAttributePost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **payload** | [**MainAttributeRewardPayload**](MainAttributeRewardPayload.md)| Voucher creation payload |

### Return type

[**MainRewardAttribution**](MainRewardAttribution.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyOfferProgramsPidRewardsRedeemPost"></a>
# **loyaltyOfferProgramsPidRewardsRedeemPost**
> MainRedeem loyaltyOfferProgramsPidRewardsRedeemPost(pid, payload)

Create redeem voucher request

Creates a request to redeem a voucher.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
MainCreateRedeemPayload payload = new MainCreateRedeemPayload(); // MainCreateRedeemPayload | Redeem transaction creation payload
try {
    MainRedeem result = apiInstance.loyaltyOfferProgramsPidRewardsRedeemPost(pid, payload);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#loyaltyOfferProgramsPidRewardsRedeemPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **payload** | [**MainCreateRedeemPayload**](MainCreateRedeemPayload.md)| Redeem transaction creation payload |

### Return type

[**MainRedeem**](MainRedeem.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyOfferProgramsPidRewardsRedeemTidCompletePost"></a>
# **loyaltyOfferProgramsPidRewardsRedeemTidCompletePost**
> MainRedeem loyaltyOfferProgramsPidRewardsRedeemTidCompletePost(pid, tid)

Complete redeem voucher request

Completes voucher redeem request.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
String tid = "tid_example"; // String | Redeem transaction ID
try {
    MainRedeem result = apiInstance.loyaltyOfferProgramsPidRewardsRedeemTidCompletePost(pid, tid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#loyaltyOfferProgramsPidRewardsRedeemTidCompletePost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **tid** | **String**| Redeem transaction ID |

### Return type

[**MainRedeem**](MainRedeem.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyOfferProgramsPidRewardsRevokeDelete"></a>
# **loyaltyOfferProgramsPidRewardsRevokeDelete**
> String loyaltyOfferProgramsPidRewardsRevokeDelete(pid, attributedRewardIds)

Revoke vouchers

Revoke attributed vouchers.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
String attributedRewardIds = "attributedRewardIds_example"; // String | Reward Attribution IDs (comma seperated)
try {
    String result = apiInstance.loyaltyOfferProgramsPidRewardsRevokeDelete(pid, attributedRewardIds);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#loyaltyOfferProgramsPidRewardsRevokeDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **attributedRewardIds** | **String**| Reward Attribution IDs (comma seperated) | [optional]

### Return type

**String**

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyOfferProgramsPidRewardsRidGet"></a>
# **loyaltyOfferProgramsPidRewardsRidGet**
> MainReward loyaltyOfferProgramsPidRewardsRidGet(pid, rid, version)

Get reward information

Returns reward information.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
UUID rid = new UUID(); // UUID | Reward ID
String version = "draft"; // String | Version
try {
    MainReward result = apiInstance.loyaltyOfferProgramsPidRewardsRidGet(pid, rid, version);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#loyaltyOfferProgramsPidRewardsRidGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **rid** | [**UUID**](.md)| Reward ID |
 **version** | **String**| Version | [optional] [default to draft] [enum: active, draft]

### Return type

[**MainReward**](MainReward.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyOfferProgramsPidRewardsValidatePost"></a>
# **loyaltyOfferProgramsPidRewardsValidatePost**
> MainRewardValidate loyaltyOfferProgramsPidRewardsValidatePost(pid, body)

Validate a reward

Validates a reward.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
MainValidateRewardPayload body = new MainValidateRewardPayload(); // MainValidateRewardPayload | Reward validation payload
try {
    MainRewardValidate result = apiInstance.loyaltyOfferProgramsPidRewardsValidatePost(pid, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#loyaltyOfferProgramsPidRewardsValidatePost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **body** | [**MainValidateRewardPayload**](MainValidateRewardPayload.md)| Reward validation payload |

### Return type

[**MainRewardValidate**](MainRewardValidate.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="loyaltyOfferProgramsPidVouchersGet"></a>
# **loyaltyOfferProgramsPidVouchersGet**
> MainModelContactRewardsResp loyaltyOfferProgramsPidVouchersGet(pid, contactId, limit, offset, sort, sortField, metadataKeyValue, rewardId)

Get voucher for a contact

Get voucher for a contact

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.RewardApi;

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

RewardApi apiInstance = new RewardApi();
UUID pid = new UUID(); // UUID | Loyalty Program ID
Integer contactId = 56; // Integer | Contact ID
Integer limit = 25; // Integer | Page size
Integer offset = 0; // Integer | Pagination offset
String sort = "desc"; // String | Sort order
String sortField = "updatedAt"; // String | Sort field
String metadataKeyValue = "metadataKeyValue_example"; // String | Metadata value for a Key filter
String rewardId = "rewardId_example"; // String | Reward ID
try {
    MainModelContactRewardsResp result = apiInstance.loyaltyOfferProgramsPidVouchersGet(pid, contactId, limit, offset, sort, sortField, metadataKeyValue, rewardId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RewardApi#loyaltyOfferProgramsPidVouchersGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pid** | [**UUID**](.md)| Loyalty Program ID |
 **contactId** | **Integer**| Contact ID |
 **limit** | **Integer**| Page size | [optional] [default to 25]
 **offset** | **Integer**| Pagination offset | [optional] [default to 0]
 **sort** | **String**| Sort order | [optional] [default to desc] [enum: asc, desc]
 **sortField** | **String**| Sort field | [optional] [default to updatedAt] [enum: updatedAt, createdAt]
 **metadataKeyValue** | **String**| Metadata value for a Key filter | [optional]
 **rewardId** | **String**| Reward ID | [optional]

### Return type

[**MainModelContactRewardsResp**](MainModelContactRewardsResp.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

