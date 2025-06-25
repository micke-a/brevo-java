
# TransactionHistory

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | [**BigDecimal**](BigDecimal.md) | The transaction amount. |  [optional]
**balanceExpirationDate** | **String** | Expiration date of the balance associated with this transaction. |  [optional]
**cancelledAt** | **String** | Timestamp when the transaction was canceled, if applicable. |  [optional]
**completedAt** | **String** | Timestamp when the transaction was successfully completed. |  [optional]
**createdAt** | **String** | Timestamp when the transaction was initiated. |  [optional]
**id** | **String** | Unique identifier of the transaction. |  [optional]
**meta** | **Object** | Optional metadata associated with the transaction. |  [optional]
**rejectReason** | **String** | Reason for rejection, if the transaction was declined. |  [optional]
**rejectedAt** | **String** | Timestamp when the transaction was rejected. |  [optional]
**status** | **String** | Current status of the transaction (e.g., pending, completed, rejected). |  [optional]



