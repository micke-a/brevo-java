
# MainOrderPayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | [**BigDecimal**](BigDecimal.md) | Total amount of the order |  [optional]
**billing** | **Object** | Billing information for the order |  [optional]
**contactId** | **Long** | Unique identifier for the contact |  [optional]
**coupons** | **List&lt;String&gt;** | List of coupon codes applied to the order |  [optional]
**createdAt** | [**OffsetDateTime**] | Timestamp when the order was created |  [optional]
**email** | **String** | Email address associated with the order |  [optional]
**id** | **String** | Unique identifier for the order |  [optional]
**identifiers** | **Object** | Additional identifiers for the order |  [optional]
**products** | [**List&lt;MainProductPayload&gt;**](MainProductPayload.md) | List of products in the order |  [optional]
**status** | **String** | Current status of the order |  [optional]
**storeId** | **String** | Identifier for the store where the order was placed |  [optional]
**updatedAt** | [**OffsetDateTime**] | Timestamp when the order was last updated |  [optional]



