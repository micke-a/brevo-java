
# ContactErrorModel

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | [**CodeEnum**](#CodeEnum) | Error code displayed in case of a failure | 
**message** | **String** | Readable message associated to the failure | 
**metadata** | **Object** | Additional information about the error |  [optional]


<a name="CodeEnum"></a>
## Enum: CodeEnum
Name | Value
---- | -----
INVALID_PARAMETER | &quot;invalid_parameter&quot;
MISSING_PARAMETER | &quot;missing_parameter&quot;
DOCUMENT_NOT_FOUND | &quot;document_not_found&quot;
ACCOUNT_IN_PROCESS | &quot;account_in_process&quot;
DUPLICATE_PARAMETER | &quot;duplicate_parameter&quot;
METHOD_NOT_ALLOWED | &quot;method_not_allowed&quot;
OUT_OF_RANGE | &quot;out_of_range&quot;



