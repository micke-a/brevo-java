
# Transaction

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | [**BigDecimal**](BigDecimal.md) | The transaction amount. |  [optional]
**balanceDefinitionId** | **String** | Unique identifier (UUID) of the associated balance definition. |  [optional]
**cancelledAt** | **String** | Timestamp when the transaction was canceled (nullable). |  [optional]
**completedAt** | **String** | Timestamp when the transaction was completed (nullable). |  [optional]
**contactId** | **Integer** | Unique identifier of the contact associated with the transaction. |  [optional]
**createdAt** | **String** | Timestamp when the transaction was created. |  [optional]
**eventTime** | **String** | Optional timestamp indicating when the transaction event occurred. |  [optional]
**expirationDate** | **String** | Expiry date of the transaction (nullable). |  [optional]
**id** | **String** | Unique identifier (UUID) of the transaction. |  [optional]
**loyaltyProgramId** | **String** | Unique identifier (UUID) of the associated loyalty program. |  [optional]
**meta** | **Object** | Optional metadata associated with the transaction. |  [optional]
**rejectReason** | **String** | Reason for rejection if the transaction was declined (nullable). |  [optional]
**rejectedAt** | **String** | Timestamp when the transaction was rejected (nullable). |  [optional]
**status** | **String** | The current status of the transaction (e.g., pending, completed, rejected). |  [optional]
**updatedAt** | **String** | Timestamp when the transaction was last updated. |  [optional]



