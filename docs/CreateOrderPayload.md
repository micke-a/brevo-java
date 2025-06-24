
# CreateOrderPayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | [**BigDecimal**](BigDecimal.md) | Order amount (must be non-zero). | 
**balanceDefinitionId** | **String** | Unique identifier (UUID) of the associated balance definition. | 
**contactId** | **Integer** | Unique identifier of the contact placing the order (must be ≥ 1). | 
**dueAt** | **String** | RFC3339 timestamp specifying when the order is due. | 
**expiresAt** | **String** | Optional RFC3339 timestamp defining order expiration. |  [optional]
**meta** | **Object** | Optional metadata associated with the order. |  [optional]
**source** | **String** | Specifies the origin of the order (&#x60;engine&#x60; or &#x60;user&#x60;). | 



