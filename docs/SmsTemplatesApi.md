# SmsTemplatesApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSMSTemplates**](SmsTemplatesApi.md#getSMSTemplates) | **GET** /transactionalSMS/templates | Return all your created SMS templates


<a name="getSMSTemplates"></a>
# **getSMSTemplates**
> InlineResponse200 getSMSTemplates(limit, offset, sort)

Return all your created SMS templates

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.SmsTemplatesApi;

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

SmsTemplatesApi apiInstance = new SmsTemplatesApi();
Long limit = 50L; // Long | Number of documents returned per page
Long offset = 0L; // Long | Index of the first document in the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
try {
    InlineResponse200 result = apiInstance.getSMSTemplates(limit, offset, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SmsTemplatesApi#getSMSTemplates");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents returned per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document in the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

