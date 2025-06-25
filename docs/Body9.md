
# Body9

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **String** | The label for the attribute (max 50 characters, cannot be empty) | 
**attributeType** | [**AttributeTypeEnum**](#AttributeTypeEnum) | The type of attribute (must be one of the defined enums) | 
**description** | **String** | A description of the attribute |  [optional]
**optionsLabels** | **List&lt;String&gt;** | Options for multi-choice or single-select attributes |  [optional]
**objectType** | [**ObjectTypeEnum**](#ObjectTypeEnum) | The type of object the attribute belongs to (prefilled with &#x60;companies&#x60;or &#x60;deal&#x60;, mandatory) | 


<a name="AttributeTypeEnum"></a>
## Enum: AttributeTypeEnum
Name | Value
---- | -----
TEXT | &quot;text&quot;
USER | &quot;user&quot;
NUMBER | &quot;number&quot;
SINGLE_SELECT | &quot;single-select&quot;
DATE | &quot;date&quot;
BOOLEAN | &quot;boolean&quot;
MULTI_CHOICE | &quot;multi-choice&quot;


<a name="ObjectTypeEnum"></a>
## Enum: ObjectTypeEnum
Name | Value
---- | -----
COMPANIES | &quot;companies&quot;
DEALS | &quot;deals&quot;



