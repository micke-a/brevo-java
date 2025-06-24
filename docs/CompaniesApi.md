# CompaniesApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**companiesGet**](CompaniesApi.md#companiesGet) | **GET** /companies | Get all companies
[**companiesIdDelete**](CompaniesApi.md#companiesIdDelete) | **DELETE** /companies/{id} | Delete a company
[**companiesIdGet**](CompaniesApi.md#companiesIdGet) | **GET** /companies/{id} | Get a company
[**companiesIdPatch**](CompaniesApi.md#companiesIdPatch) | **PATCH** /companies/{id} | Update a company
[**companiesImportPost**](CompaniesApi.md#companiesImportPost) | **POST** /companies/import | Import companies(creation and updation)
[**companiesLinkUnlinkIdPatch**](CompaniesApi.md#companiesLinkUnlinkIdPatch) | **PATCH** /companies/link-unlink/{id} | Link and Unlink company with contacts and deals
[**companiesPost**](CompaniesApi.md#companiesPost) | **POST** /companies | Create a company
[**crmAttributesCompaniesGet**](CompaniesApi.md#crmAttributesCompaniesGet) | **GET** /crm/attributes/companies | Get company attributes
[**crmAttributesPost**](CompaniesApi.md#crmAttributesPost) | **POST** /crm/attributes | Create a deal/company attribute


<a name="companiesGet"></a>
# **companiesGet**
> CompaniesList companiesGet(filters, linkedContactsIds, linkedDealsIds, modifiedSince, createdSince, page, limit, sort, sortBy)

Get all companies

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CompaniesApi;

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

CompaniesApi apiInstance = new CompaniesApi();
String filters = "filters_example"; // String | Filter by attrbutes. If you have filter for owner on your side please send it as {\"attributes.owner\":\"5b1a17d914b73d35a76ca0c7\"}
Long linkedContactsIds = 789L; // Long | Filter by linked contacts ids
String linkedDealsIds = "linkedDealsIds_example"; // String | Filter by linked deals ids
String modifiedSince = "modifiedSince_example"; // String | Filter (urlencoded) the contacts modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result.
String createdSince = "createdSince_example"; // String | Filter (urlencoded) the contacts created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result.
Long page = 789L; // Long | Index of the first document of the page
Long limit = 50L; // Long | Number of documents per page
String sort = "sort_example"; // String | Sort the results in the ascending/descending order. Default order is **descending** by creation if `sort` is not passed
String sortBy = "sortBy_example"; // String | The field used to sort field names.
try {
    CompaniesList result = apiInstance.companiesGet(filters, linkedContactsIds, linkedDealsIds, modifiedSince, createdSince, page, limit, sort, sortBy);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CompaniesApi#companiesGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filters** | **String**| Filter by attrbutes. If you have filter for owner on your side please send it as {&quot;attributes.owner&quot;:&quot;5b1a17d914b73d35a76ca0c7&quot;} | [optional]
 **linkedContactsIds** | **Long**| Filter by linked contacts ids | [optional]
 **linkedDealsIds** | **String**| Filter by linked deals ids | [optional]
 **modifiedSince** | **String**| Filter (urlencoded) the contacts modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result. | [optional]
 **createdSince** | **String**| Filter (urlencoded) the contacts created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result. | [optional]
 **page** | **Long**| Index of the first document of the page | [optional]
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **sort** | **String**| Sort the results in the ascending/descending order. Default order is **descending** by creation if &#x60;sort&#x60; is not passed | [optional] [enum: asc, desc]
 **sortBy** | **String**| The field used to sort field names. | [optional]

### Return type

[**CompaniesList**](CompaniesList.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="companiesIdDelete"></a>
# **companiesIdDelete**
> companiesIdDelete(id)

Delete a company

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CompaniesApi;

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

CompaniesApi apiInstance = new CompaniesApi();
String id = "id_example"; // String | 
try {
    apiInstance.companiesIdDelete(id);
} catch (ApiException e) {
    System.err.println("Exception when calling CompaniesApi#companiesIdDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="companiesIdGet"></a>
# **companiesIdGet**
> Company companiesIdGet(id)

Get a company

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CompaniesApi;

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

CompaniesApi apiInstance = new CompaniesApi();
String id = "id_example"; // String | 
try {
    Company result = apiInstance.companiesIdGet(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CompaniesApi#companiesIdGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |

### Return type

[**Company**](Company.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="companiesIdPatch"></a>
# **companiesIdPatch**
> Company companiesIdPatch(id, body)

Update a company

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CompaniesApi;

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

CompaniesApi apiInstance = new CompaniesApi();
String id = "id_example"; // String | 
Body7 body = new Body7(); // Body7 | Updated company details.
try {
    Company result = apiInstance.companiesIdPatch(id, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CompaniesApi#companiesIdPatch");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |
 **body** | [**Body7**](Body7.md)| Updated company details. |

### Return type

[**Company**](Company.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="companiesImportPost"></a>
# **companiesImportPost**
> InlineResponse2004 companiesImportPost(file, mapping)

Import companies(creation and updation)

Import companies from a CSV file with mapping options.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CompaniesApi;

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

CompaniesApi apiInstance = new CompaniesApi();
File file = new File("/path/to/file.txt"); // File | The CSV file to upload.The file should have the first row as the mapping attribute. Some default attribute names are (a) company_id [brevo mongoID to update deals] (b) associated_contact (c) associated_deal (f) any other attribute with internal name 
String mapping = "mapping_example"; // String | The mapping options in Json format.   json    {       \"link_entities\": true, // Determines whether to link related entities during the import process       \"unlink_entities\": false, //Determines whether to unlink related entities during the import process.       \"update_existing_records\": true, // Determines whether to update based on company ID or treat every row as create       \"unset_empty_attributes\": false // Determines whether unset a specific attribute during update if values input is blank       \"use_company_identifier\": false // Determines whether to use company name as identifier     } 
try {
    InlineResponse2004 result = apiInstance.companiesImportPost(file, mapping);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CompaniesApi#companiesImportPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **File**| The CSV file to upload.The file should have the first row as the mapping attribute. Some default attribute names are (a) company_id [brevo mongoID to update deals] (b) associated_contact (c) associated_deal (f) any other attribute with internal name  |
 **mapping** | **String**| The mapping options in JSON format.   json    {       &quot;link_entities&quot;: true, // Determines whether to link related entities during the import process       &quot;unlink_entities&quot;: false, //Determines whether to unlink related entities during the import process.       &quot;update_existing_records&quot;: true, // Determines whether to update based on company ID or treat every row as create       &quot;unset_empty_attributes&quot;: false // Determines whether unset a specific attribute during update if values input is blank       &quot;use_company_identifier&quot;: false // Determines whether to use company name as identifier     }  |

### Return type

[**InlineResponse2004**](InlineResponse2004.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="companiesLinkUnlinkIdPatch"></a>
# **companiesLinkUnlinkIdPatch**
> companiesLinkUnlinkIdPatch(id, body)

Link and Unlink company with contacts and deals

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CompaniesApi;

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

CompaniesApi apiInstance = new CompaniesApi();
String id = "id_example"; // String | 
Body8 body = new Body8(); // Body8 | Linked / Unlinked contacts and deals ids.
try {
    apiInstance.companiesLinkUnlinkIdPatch(id, body);
} catch (ApiException e) {
    System.err.println("Exception when calling CompaniesApi#companiesLinkUnlinkIdPatch");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |
 **body** | [**Body8**](Body8.md)| Linked / Unlinked contacts and deals ids. |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="companiesPost"></a>
# **companiesPost**
> InlineResponse2002 companiesPost(body)

Create a company

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CompaniesApi;

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

CompaniesApi apiInstance = new CompaniesApi();
Body6 body = new Body6(); // Body6 | Company create data.
try {
    InlineResponse2002 result = apiInstance.companiesPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CompaniesApi#companiesPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Body6**](Body6.md)| Company create data. |

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmAttributesCompaniesGet"></a>
# **crmAttributesCompaniesGet**
> CompanyAttributes crmAttributesCompaniesGet()

Get company attributes

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CompaniesApi;

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

CompaniesApi apiInstance = new CompaniesApi();
try {
    CompanyAttributes result = apiInstance.crmAttributesCompaniesGet();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CompaniesApi#crmAttributesCompaniesGet");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CompanyAttributes**](CompanyAttributes.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmAttributesPost"></a>
# **crmAttributesPost**
> InlineResponse2003 crmAttributesPost(body)

Create a deal/company attribute

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CompaniesApi;

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

CompaniesApi apiInstance = new CompaniesApi();
Body9 body = new Body9(); // Body9 | Attribute creation data for company
try {
    InlineResponse2003 result = apiInstance.crmAttributesPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CompaniesApi#crmAttributesPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Body9**](Body9.md)| Attribute creation data for company |

### Return type

[**InlineResponse2003**](InlineResponse2003.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

