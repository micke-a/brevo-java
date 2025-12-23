# CustomObjectsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getrecords**](CustomObjectsApi.md#getrecords) | **GET** /objects/{object_type}/records | Get the list of object records and total records count for an object.
[**upsertrecords**](CustomObjectsApi.md#upsertrecords) | **POST** /objects/{object_type}/batch/upsert | Create/Update object records in bulk


<a name="getrecords"></a>
# **getrecords**
> getrecords(objectType, limit, pageNum, sort, association)

Get the list of object records and total records count for an object.

This API retrieves a list of object records along with their associated records and provides the total count of records for the specified object.  **Note**: Contact as object type is not supported in this endpoint. 

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CustomObjectsApi;

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

CustomObjectsApi apiInstance = new CustomObjectsApi();
Object objectType = null; // Object | object type for the attribute
Object limit = null; // Object | Number of records returned per page
Object pageNum = null; // Object | Page number for pagination. It's used to fetch the object records on a provided page number. Must be a valid positive integer.
Object sort = null; // Object | Sort order, must be 'asc' or 'desc'. Default to 'desc' if not provided.
Object association = null; // Object | Whether to include associations, must be 'true' or 'false'. Default to 'false' if not provided.
try {
    apiInstance.getrecords(objectType, limit, pageNum, sort, association);
} catch (ApiException e) {
    System.err.println("Exception when calling CustomObjectsApi#getrecords");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **objectType** | [**Object**](.md)| object type for the attribute |
 **limit** | [**Object**](.md)| Number of records returned per page |
 **pageNum** | [**Object**](.md)| Page number for pagination. It&#39;s used to fetch the object records on a provided page number. Must be a valid positive integer. |
 **sort** | [**Object**](.md)| Sort order, must be &#39;asc&#39; or &#39;desc&#39;. Default to &#39;desc&#39; if not provided. | [optional]
 **association** | [**Object**](.md)| Whether to include associations, must be &#39;true&#39; or &#39;false&#39;. Default to &#39;false&#39; if not provided. | [optional]

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="upsertrecords"></a>
# **upsertrecords**
> upsertrecords(objectType)

Create/Update object records in bulk

This API allows bulk upsert of object records in a single request. Each object record may include   - Attributes   - Identifiers   - Associations  **Response:**   The API processes the request asynchronously and returns a processId that you can use to track the background process status.  **API and Schema Limitation:**   - Size:       - Max 1000 objects records per request       - Max request body size: 1 MB    - Max 500 attributes defined per object record upsert request     - This is coherent with schema limitation: an object cannot have more than 500 attributes.     - Worth noting: Nothing happens If an attribute is mentioned in the request, but was not previously defined for the object schema (no error, no attribute creation)    - Max 10 associations defined per object record upsert request     - This is coherent with schema limitation: an object cannot have more than 10 associations with other objects. and each object record can be linked to max 10 other records.  **Errors:**     - Make sure both object records exist before associating them, else the API will return an error.     - This route does not create objects. The object where the object records are upserted by this API must be created already else the API will return an error &quot;invalid object type&quot;. 

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CustomObjectsApi;

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

CustomObjectsApi apiInstance = new CustomObjectsApi();
Object objectType = null; // Object | object type for the attribute
try {
    apiInstance.upsertrecords(objectType);
} catch (ApiException e) {
    System.err.println("Exception when calling CustomObjectsApi#upsertrecords");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **objectType** | [**Object**](.md)| object type for the attribute |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

