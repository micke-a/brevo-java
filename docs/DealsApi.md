# DealsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**crmAttributesDealsGet**](DealsApi.md#crmAttributesDealsGet) | **GET** /crm/attributes/deals | Get deal attributes
[**crmAttributesPost**](DealsApi.md#crmAttributesPost) | **POST** /crm/attributes | Create a deal/company attribute
[**crmDealsGet**](DealsApi.md#crmDealsGet) | **GET** /crm/deals | Get all deals
[**crmDealsIdDelete**](DealsApi.md#crmDealsIdDelete) | **DELETE** /crm/deals/{id} | Delete a deal
[**crmDealsIdGet**](DealsApi.md#crmDealsIdGet) | **GET** /crm/deals/{id} | Get a deal
[**crmDealsIdPatch**](DealsApi.md#crmDealsIdPatch) | **PATCH** /crm/deals/{id} | Update a deal
[**crmDealsImportPost**](DealsApi.md#crmDealsImportPost) | **POST** /crm/deals/import | Import deals(creation and updation)
[**crmDealsLinkUnlinkIdPatch**](DealsApi.md#crmDealsLinkUnlinkIdPatch) | **PATCH** /crm/deals/link-unlink/{id} | Link and Unlink a deal with contacts and companies
[**crmDealsPost**](DealsApi.md#crmDealsPost) | **POST** /crm/deals | Create a deal
[**crmPipelineDetailsAllGet**](DealsApi.md#crmPipelineDetailsAllGet) | **GET** /crm/pipeline/details/all | Get all pipelines
[**crmPipelineDetailsGet**](DealsApi.md#crmPipelineDetailsGet) | **GET** /crm/pipeline/details | Get pipeline stages
[**crmPipelineDetailsPipelineIDGet**](DealsApi.md#crmPipelineDetailsPipelineIDGet) | **GET** /crm/pipeline/details/{pipelineID} | Get a pipeline


<a name="crmAttributesDealsGet"></a>
# **crmAttributesDealsGet**
> DealAttributes crmAttributesDealsGet()

Get deal attributes

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
try {
    DealAttributes result = apiInstance.crmAttributesDealsGet();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmAttributesDealsGet");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**DealAttributes**](DealAttributes.md)

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
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
Body9 body = new Body9(); // Body9 | Attribute creation data for company
try {
    InlineResponse2003 result = apiInstance.crmAttributesPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmAttributesPost");
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

<a name="crmDealsGet"></a>
# **crmDealsGet**
> DealsList crmDealsGet(filtersAttributesDealName, filtersLinkedCompaniesIds, filtersLinkedContactsIds, modifiedSince, createdSince, offset, limit, sort, sortBy)

Get all deals

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String filtersAttributesDealName = "filtersAttributesDealName_example"; // String | Filter by attributes. If you have a filter for the owner on your end, please send it as filters[attributes.deal_owner] and utilize the account email for the filtering.
String filtersLinkedCompaniesIds = "filtersLinkedCompaniesIds_example"; // String | Filter by linked companies ids
String filtersLinkedContactsIds = "filtersLinkedContactsIds_example"; // String | Filter by linked companies ids
String modifiedSince = "modifiedSince_example"; // String | Filter (urlencoded) the contacts modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result.
String createdSince = "createdSince_example"; // String | Filter (urlencoded) the contacts created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result.
Long offset = 789L; // Long | Index of the first document of the page
Long limit = 50L; // Long | Number of documents per page
String sort = "sort_example"; // String | Sort the results in the ascending/descending order. Default order is **descending** by creation if `sort` is not passed
String sortBy = "sortBy_example"; // String | The field used to sort field names.
try {
    DealsList result = apiInstance.crmDealsGet(filtersAttributesDealName, filtersLinkedCompaniesIds, filtersLinkedContactsIds, modifiedSince, createdSince, offset, limit, sort, sortBy);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filtersAttributesDealName** | **String**| Filter by attributes. If you have a filter for the owner on your end, please send it as filters[attributes.deal_owner] and utilize the account email for the filtering. | [optional]
 **filtersLinkedCompaniesIds** | **String**| Filter by linked companies ids | [optional]
 **filtersLinkedContactsIds** | **String**| Filter by linked companies ids | [optional]
 **modifiedSince** | **String**| Filter (urlencoded) the contacts modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result. | [optional]
 **createdSince** | **String**| Filter (urlencoded) the contacts created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result. | [optional]
 **offset** | **Long**| Index of the first document of the page | [optional]
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **sort** | **String**| Sort the results in the ascending/descending order. Default order is **descending** by creation if &#x60;sort&#x60; is not passed | [optional] [enum: asc, desc]
 **sortBy** | **String**| The field used to sort field names. | [optional]

### Return type

[**DealsList**](DealsList.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsIdDelete"></a>
# **crmDealsIdDelete**
> crmDealsIdDelete(id)

Delete a deal

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String id = "id_example"; // String | 
try {
    apiInstance.crmDealsIdDelete(id);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsIdDelete");
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

<a name="crmDealsIdGet"></a>
# **crmDealsIdGet**
> Deal crmDealsIdGet(id)

Get a deal

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String id = "id_example"; // String | 
try {
    Deal result = apiInstance.crmDealsIdGet(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsIdGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |

### Return type

[**Deal**](Deal.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsIdPatch"></a>
# **crmDealsIdPatch**
> crmDealsIdPatch(id, body)

Update a deal

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String id = "id_example"; // String | 
Body11 body = new Body11(); // Body11 | Updated deal details.
try {
    apiInstance.crmDealsIdPatch(id, body);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsIdPatch");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |
 **body** | [**Body11**](Body11.md)| Updated deal details. |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsImportPost"></a>
# **crmDealsImportPost**
> InlineResponse2004 crmDealsImportPost(file, mapping)

Import deals(creation and updation)

Import deals from a CSV file with mapping options.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
File file = new File("/path/to/file.txt"); // File | The CSV file to upload.The file should have the first row as the mapping attribute. Some default attribute names are (a) deal_id [brevo mongoID to update deals] (b) associated_contact (c) associated_company (f) any other attribute with internal name 
String mapping = "mapping_example"; // String | The mapping options in Json format.   json    {       \"link_entities\": true, // Determines whether to link related entities during the import process       \"unlink_entities\": false, //Determines whether to unlink related entities during the import process.       \"update_existing_records\": true, // Determines whether to update based on deal ID or treat every row as create       \"unset_empty_attributes\": false // Determines whether unset a specific attribute during update if values input is blank     } 
try {
    InlineResponse2004 result = apiInstance.crmDealsImportPost(file, mapping);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsImportPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **File**| The CSV file to upload.The file should have the first row as the mapping attribute. Some default attribute names are (a) deal_id [brevo mongoID to update deals] (b) associated_contact (c) associated_company (f) any other attribute with internal name  |
 **mapping** | **String**| The mapping options in JSON format.   json    {       &quot;link_entities&quot;: true, // Determines whether to link related entities during the import process       &quot;unlink_entities&quot;: false, //Determines whether to unlink related entities during the import process.       &quot;update_existing_records&quot;: true, // Determines whether to update based on deal ID or treat every row as create       &quot;unset_empty_attributes&quot;: false // Determines whether unset a specific attribute during update if values input is blank     }  |

### Return type

[**InlineResponse2004**](InlineResponse2004.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="crmDealsLinkUnlinkIdPatch"></a>
# **crmDealsLinkUnlinkIdPatch**
> crmDealsLinkUnlinkIdPatch(id, body)

Link and Unlink a deal with contacts and companies

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String id = "id_example"; // String | 
Body12 body = new Body12(); // Body12 | Linked / Unlinked contacts and companies ids.
try {
    apiInstance.crmDealsLinkUnlinkIdPatch(id, body);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsLinkUnlinkIdPatch");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |
 **body** | [**Body12**](Body12.md)| Linked / Unlinked contacts and companies ids. |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsPost"></a>
# **crmDealsPost**
> InlineResponse2011 crmDealsPost(body)

Create a deal

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
Body10 body = new Body10(); // Body10 | Deal create data.
try {
    InlineResponse2011 result = apiInstance.crmDealsPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Body10**](Body10.md)| Deal create data. |

### Return type

[**InlineResponse2011**](InlineResponse2011.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmPipelineDetailsAllGet"></a>
# **crmPipelineDetailsAllGet**
> Pipelines crmPipelineDetailsAllGet()

Get all pipelines

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
try {
    Pipelines result = apiInstance.crmPipelineDetailsAllGet();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmPipelineDetailsAllGet");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Pipelines**](Pipelines.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmPipelineDetailsGet"></a>
# **crmPipelineDetailsGet**
> Pipeline crmPipelineDetailsGet()

Get pipeline stages

This endpoint is deprecated. Prefer /crm/pipeline/details/{pipelineID} instead.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
try {
    Pipeline result = apiInstance.crmPipelineDetailsGet();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmPipelineDetailsGet");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Pipeline**](Pipeline.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmPipelineDetailsPipelineIDGet"></a>
# **crmPipelineDetailsPipelineIDGet**
> Pipelines crmPipelineDetailsPipelineIDGet(pipelineID)

Get a pipeline

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String pipelineID = "pipelineID_example"; // String | 
try {
    Pipelines result = apiInstance.crmPipelineDetailsPipelineIDGet(pipelineID);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmPipelineDetailsPipelineIDGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pipelineID** | **String**|  |

### Return type

[**Pipelines**](Pipelines.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

