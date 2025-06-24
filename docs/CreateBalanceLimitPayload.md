
# CreateBalanceLimitPayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**constraintType** | [**ConstraintTypeEnum**](#ConstraintTypeEnum) | Defines whether the limit applies to transaction count or amount. | 
**durationUnit** | [**DurationUnitEnum**](#DurationUnitEnum) | Unit of time for which the limit is applicable. | 
**durationValue** | **Integer** | Number of time units for the balance limit. | 
**slidingSchedule** | **Boolean** | Determines if the limit resets on a rolling schedule. |  [optional]
**transactionType** | [**TransactionTypeEnum**](#TransactionTypeEnum) | Specifies whether the limit applies to credit or debit transactions. | 
**value** | **Integer** | Maximum allowed value for the specified constraint type. | 


<a name="ConstraintTypeEnum"></a>
## Enum: ConstraintTypeEnum
Name | Value
---- | -----
TRANSACTION | &quot;transaction&quot;
AMOUNT | &quot;amount&quot;


<a name="DurationUnitEnum"></a>
## Enum: DurationUnitEnum
Name | Value
---- | -----
DAY | &quot;day&quot;
WEEK | &quot;week&quot;
MONTH | &quot;month&quot;
YEAR | &quot;year&quot;


<a name="TransactionTypeEnum"></a>
## Enum: TransactionTypeEnum
Name | Value
---- | -----
CREDIT | &quot;credit&quot;
DEBIT | &quot;debit&quot;



