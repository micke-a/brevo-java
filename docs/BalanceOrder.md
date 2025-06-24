
# BalanceOrder

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | [**BigDecimal**](BigDecimal.md) | Order amount (must not be zero). | 
**balanceDefinitionId** | **String** | Optional unique identifier (UUID) of the associated balance definition. |  [optional]
**contactId** | **Integer** | Unique identifier of the contact placing the order (must be ≥ 1). | 
**createdAt** | **String** | RFC3339 timestamp indicating when the order was created. | 
**dueAt** | **String** | RFC3339 timestamp specifying when the order is due in the future. | 
**expiresAt** | **String** | Optional RFC3339 timestamp defining order expiration in the future. |  [optional]
**id** | **String** | Unique identifier for the balance order. |  [optional]
**loyaltyProgramId** | **String** | Unique identifier of the loyalty program associated with the order. | 
**meta** | **Object** | Optional metadata associated with the order. |  [optional]
**processedAt** | **String** | Optional RFC3339 timestamp indicating when the order was processed. |  [optional]
**transactionid** | **String** | Optional reference to the associated transaction ID. |  [optional]
**updatedAt** | **String** | RFC3339 timestamp indicating the last update to the order. | 



