
# CreateAttribute

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **String** | Value of the attribute. Use only if the attribute&#39;s category is &#39;calculated&#39; or &#39;global&#39; |  [optional]
**isRecurring** | **Boolean** | Type of the attribute. Use only if the attribute&#39;s category is &#39;calculated&#39; or &#39;global&#39; |  [optional]
**enumeration** | [**List&lt;CreateAttributeEnumeration&gt;**](CreateAttributeEnumeration.md) | List of values and labels that the attribute can take. Use only if the attribute&#39;s category is &quot;category&quot;. None of the category options can exceed max 200 characters. For example, [{&quot;value&quot;:1, &quot;label&quot;:&quot;male&quot;}, {&quot;value&quot;:2, &quot;label&quot;:&quot;female&quot;}] |  [optional]
**multiCategoryOptions** | **List&lt;String&gt;** | List of options you want to add for multiple-choice attribute. **Use only if the attribute&#39;s category is &quot;normal&quot; and attribute&#39;s type is &quot;multiple-choice&quot;. None of the multicategory options can exceed max 200 characters.** For example: **[&quot;USA&quot;,&quot;INDIA&quot;]**  |  [optional]
**type** | [**TypeEnum**](#TypeEnum) | Type of the attribute. Use only if the attribute&#39;s category is &#39;normal&#39;, &#39;category&#39; or &#39;transactional&#39; ( type &#39;user&#39; and &#39;multiple-choice&#39; is only available if the category is &#39;normal&#39; attribute, type &#39;id&#39; is only available if the category is &#39;transactional&#39; attribute &amp; type &#39;category&#39; is only available if the category is &#39;category&#39; attribute ) |  [optional]


<a name="TypeEnum"></a>
## Enum: TypeEnum
Name | Value
---- | -----
TEXT | &quot;text&quot;
DATE | &quot;date&quot;
FLOAT | &quot;float&quot;
BOOLEAN | &quot;boolean&quot;
ID | &quot;id&quot;
CATEGORY | &quot;category&quot;
MULTIPLE_CHOICE | &quot;multiple-choice&quot;



