
# BalanceLimit

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**balanceDefinitionId** | **String** | balance definition ID |  [optional]
**constraintType** | **String** | Defines the type of constraint (e.g., transaction-based or amount-based). |  [optional]
**createdAt** | **String** | Timestamp of when the balance limit was created. | 
**durationUnit** | **String** | Time unit for the balance limit (day, week, month, year). |  [optional]
**durationValue** | **Integer** | Number of time units the balance limit applies to. |  [optional]
**id** | **String** | Unique identifier for the balance limit. |  [optional]
**slidingSchedule** | **Boolean** | Indicates if the limit resets periodically based on a sliding schedule. |  [optional]
**transactionType** | **String** | Specifies whether the limit applies to credit or debit transactions. |  [optional]
**updatedAt** | **String** | Timestamp of the last update to the balance limit. | 
**value** | **Integer** | The maximum allowed value for the defined constraint. |  [optional]



