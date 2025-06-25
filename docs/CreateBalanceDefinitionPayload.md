
# CreateBalanceDefinitionPayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**balanceAvailabilityDurationModifier** | [**BalanceAvailabilityDurationModifierEnum**](#BalanceAvailabilityDurationModifierEnum) | Defines when the balance expires within the selected duration. |  [optional]
**balanceAvailabilityDurationUnit** | [**BalanceAvailabilityDurationUnitEnum**](#BalanceAvailabilityDurationUnitEnum) | Unit of time for balance validity. |  [optional]
**balanceAvailabilityDurationValue** | **Integer** | Number of time units before the balance expires. |  [optional]
**balanceExpirationDate** | [**LocalDate**] | Fixed expiration date (&#x60;dd/mm&#x60; format) as an alternative to duration-based expiry. |  [optional]
**balanceOptionAmountOvertakingStrategy** | [**BalanceOptionAmountOvertakingStrategyEnum**](#BalanceOptionAmountOvertakingStrategyEnum) | Defines whether partial credit is allowed when reaching max balance. |  [optional]
**balanceOptionCreditRounding** | [**BalanceOptionCreditRoundingEnum**](#BalanceOptionCreditRoundingEnum) | Defines rounding strategy for credit transactions. |  [optional]
**balanceOptionDebitRounding** | [**BalanceOptionDebitRoundingEnum**](#BalanceOptionDebitRoundingEnum) | Defines rounding strategy for debit transactions. |  [optional]
**description** | **String** | Short description of the balance definition. |  [optional]
**imageRef** | **String** | URL of an optional image reference. |  [optional]
**maxAmount** | [**BigDecimal**](BigDecimal.md) | Maximum allowable balance amount. |  [optional]
**maxCreditAmountLimit** | [**BigDecimal**](BigDecimal.md) | Maximum credit allowed per operation. |  [optional]
**maxDebitAmountLimit** | [**BigDecimal**](BigDecimal.md) | Maximum debit allowed per operation. |  [optional]
**meta** | **Object** | Additional metadata for the balance definition. |  [optional]
**minAmount** | [**BigDecimal**](BigDecimal.md) | Minimum allowable balance amount. |  [optional]
**name** | **String** | Name of the balance definition. | 
**unit** | [**UnitEnum**](#UnitEnum) | Unit of balance measurement. | 


<a name="BalanceAvailabilityDurationModifierEnum"></a>
## Enum: BalanceAvailabilityDurationModifierEnum
Name | Value
---- | -----
NOMODIFICATION | &quot;noModification&quot;
STARTOFPERIOD | &quot;startOfPeriod&quot;
ENDOFPERIOD | &quot;endOfPeriod&quot;


<a name="BalanceAvailabilityDurationUnitEnum"></a>
## Enum: BalanceAvailabilityDurationUnitEnum
Name | Value
---- | -----
DAY | &quot;day&quot;
WEEK | &quot;week&quot;
MONTH | &quot;month&quot;
YEAR | &quot;year&quot;


<a name="BalanceOptionAmountOvertakingStrategyEnum"></a>
## Enum: BalanceOptionAmountOvertakingStrategyEnum
Name | Value
---- | -----
STRICT | &quot;strict&quot;
PARTIAL | &quot;partial&quot;


<a name="BalanceOptionCreditRoundingEnum"></a>
## Enum: BalanceOptionCreditRoundingEnum
Name | Value
---- | -----
LOWER | &quot;lower&quot;
UPPER | &quot;upper&quot;
NATURAL | &quot;natural&quot;


<a name="BalanceOptionDebitRoundingEnum"></a>
## Enum: BalanceOptionDebitRoundingEnum
Name | Value
---- | -----
LOWER | &quot;lower&quot;
UPPER | &quot;upper&quot;
NATURAL | &quot;natural&quot;


<a name="UnitEnum"></a>
## Enum: UnitEnum
Name | Value
---- | -----
POINTS | &quot;POINTS&quot;
EUR | &quot;EUR&quot;
USD | &quot;USD&quot;
MXN | &quot;MXN&quot;
GBP | &quot;GBP&quot;
INR | &quot;INR&quot;
CAD | &quot;CAD&quot;
SGD | &quot;SGD&quot;
RON | &quot;RON&quot;
JPY | &quot;JPY&quot;
MYR | &quot;MYR&quot;
CLP | &quot;CLP&quot;
PEN | &quot;PEN&quot;
MAD | &quot;MAD&quot;
AUD | &quot;AUD&quot;
CHF | &quot;CHF&quot;
BRL | &quot;BRL&quot;



