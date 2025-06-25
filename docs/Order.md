
# Order

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Unique ID of the order. | 
**createdAt** | **String** | Event occurrence UTC date-time (YYYY-MM-DDTHH:mm:ssZ), when order is actually created. | 
**updatedAt** | **String** | Event updated UTC date-time (YYYY-MM-DDTHH:mm:ssZ), when the status of the order is actually changed/updated. | 
**status** | **String** | State of the order. | 
**amount** | [**BigDecimal**](BigDecimal.md) | Total amount of the order, including all shipping expenses, tax and the price of items. | 
**storeId** | **String** | ID of store where the order is placed |  [optional]
**identifiers** | [**OrderIdentifiers**](OrderIdentifiers.md) |  |  [optional]
**products** | [**List&lt;OrderProducts&gt;**](OrderProducts.md) |  | 
**billing** | [**OrderBilling**](OrderBilling.md) |  |  [optional]
**coupons** | **List&lt;String&gt;** | Coupons applied to the order. Stored case insensitive. |  [optional]
**metaInfo** | **Map&lt;String, Object&gt;** | Meta data of order to store additional detal such as custom message, customer type, source. |  [optional]



