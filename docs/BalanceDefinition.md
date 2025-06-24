
# BalanceDefinition

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**balanceAvailabilityDurationModifier** | [**BalanceAvailabilityDurationModifierEnum**](#BalanceAvailabilityDurationModifierEnum) | startOfPeriod depicts the balancy expiry on start of day/week/month/year. endOfPeriod depicts the balancy expiry on end of day/week/month/year |  [optional]
**balanceAvailabilityDurationUnit** | **String** | Unit of time for the balance&#39;s availability (e.g., day/week/month/year). |  [optional]
**balanceAvailabilityDurationValue** | **Integer** | Number of days/weeks/month/year for balance expiry |  [optional]
**balanceExpirationDate** | [**OffsetDateTime**] | Date when the balance expires and can no longer be used, in dd/mm format. The balance will be expired when this date appears next in the calendar and only one of balanceExpirationDate or balance availability fields can be used. |  [optional]
**balanceOptionAmountOvertakingStrategy** | **String** | Partial enables partial credit of balance if maximum balance limit is reaching. Strict enables rejection of transaction if it will breach the max credit amount limit. |  [optional]
**balanceOptionCreditRounding** | **String** | Rounding strategy for credit transactions. |  [optional]
**balanceOptionDebitRounding** | **String** | Rounding strategy for debit transactions. |  [optional]
**createdAt** | [**OffsetDateTime**] | Timestamp of balance definition creation. |  [optional]
**deletedAt** | **String** | Timestamp of balance definition deletion (nullable). |  [optional]
**description** | **String** | Short description of the balance definition. |  [optional]
**id** | **String** | Unique identifier for the balance definition. |  [optional]
**imageRef** | **String** | Optional image reference URL. |  [optional]
**maxAmount** | [**BigDecimal**](BigDecimal.md) | Maximum allowable balance. |  [optional]
**maxCreditAmountLimit** | [**BigDecimal**](BigDecimal.md) | Max credit allowed per operation. |  [optional]
**maxDebitAmountLimit** | [**BigDecimal**](BigDecimal.md) | Max debit allowed per operation. |  [optional]
**meta** | **Map&lt;String, Object&gt;** | Additional metadata for the balance definition. |  [optional]
**minAmount** | [**BigDecimal**](BigDecimal.md) | Minimum allowable balance. |  [optional]
**name** | **String** | Name of the balance definition. |  [optional]
**unit** | **String** | Unit of balance (e.g., points, currency). |  [optional]
**updatedAt** | **String** | Timestamp of the last update. |  [optional]


<a name="BalanceAvailabilityDurationModifierEnum"></a>
## Enum: BalanceAvailabilityDurationModifierEnum
Name | Value
---- | -----
STARTOFPERIOD | &quot;startOfPeriod&quot;
ENDOFPERIOD | &quot;endOfPeriod&quot;
NOMODIFICATION | &quot;noModification&quot;



