
# MainReward

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attributionPerConsumer** | **Integer** | Maximum number of times a consumer can be attributed this reward |  [optional]
**balanceDefinitionId** | [**UUID**](UUID.md) | Unique identifier for the balance definition |  [optional]
**code** | **String** | Unique code for the reward |  [optional]
**codeCount** | **Long** | Total number of codes generated |  [optional]
**codeGeneratorId** | [**UUID**](UUID.md) | Unique identifier for the code generator |  [optional]
**codePoolId** | [**UUID**](UUID.md) | Unique identifier for the code pool |  [optional]
**config** | **String** | Configuration settings for the reward |  [optional]
**createdAt** | [**OffsetDateTime**] | Timestamp when the reward was created |  [optional]
**disabledAt** | [**OffsetDateTime**] | Disabled date of the reward |  [optional]
**endDate** | [**OffsetDateTime**] | End date of the reward validity |  [optional]
**expirationDate** | [**OffsetDateTime**] | Expiration date of the reward |  [optional]
**expirationModifier** | [**ExpirationModifierEnum**](#ExpirationModifierEnum) | Select startOfPeriod to configure rewards expiry on start of day/week/month/year. Select endOfPeriod to configure reward expiry on end of day/week/month/year, else select noModification |  [optional]
**expirationUnit** | **String** | Unit of time for the rewards&#39;s availability (e.g., day/week/month/year). |  [optional]
**expirationValue** | **Integer** | Number of days/weeks/month/year for reward expiry |  [optional]
**generator** | **Object** | object |  [optional]
**id** | [**UUID**](UUID.md) | Unique identifier for the reward |  [optional]
**limits** | [**List&lt;MainLimit&gt;**](MainLimit.md) | Attribution / Redeem Limits for the reward |  [optional]
**loyaltyProgramId** | [**UUID**](UUID.md) | Id of the loyalty program to which the current reward belongs to |  [optional]
**meta** | **Map&lt;String, Object&gt;** | Additional data for reward definition |  [optional]
**name** | **String** | Name of the reward |  [optional]
**products** | [**List&lt;MainProduct&gt;**](MainProduct.md) | Selected products for reward definition |  [optional]
**publicDescription** | **String** | Public description for the reward |  [optional]
**publicImage** | **String** | Public Image for the reward |  [optional]
**publicName** | **String** | Public name for the reward |  [optional]
**redeemPerConsumer** | **Integer** | Defines the redeem limit for the consumer |  [optional]
**redeemRules** | **List&lt;String&gt;** | Rules defined to redeem a reward |  [optional]
**rewardConfigs** | **Object** | object |  [optional]
**rule** | **Object** | Rule to define the reward |  [optional]
**startDate** | [**OffsetDateTime**] | Start date of attribution of the reward |  [optional]
**subtractBalanceDefinitionId** | **String** | Id of the selected balance while redeeming / attributing a reward |  [optional]
**subtractBalanceStrategy** | **String** | Strategy of the Balance while redeeming / attributing a reward |  [optional]
**subtractBalanceValue** | **Integer** | Amount of balance to be selected while redeeming / attributing a reward |  [optional]
**subtractTotalBalance** | **Boolean** | Value to indicate to subtract full balance or not |  [optional]
**totalAttribution** | **Integer** | Defines the limit to which a consumer can attribute a reward |  [optional]
**totalRedeem** | **Integer** | Defines the limit to which a consumer can redeem a reward |  [optional]
**triggerId** | **String** | Id of the Rule to be updated for that reward |  [optional]
**unit** | **String** | Selected unit of the balance |  [optional]
**updatedAt** | **String** | Timestamp for when this reward was last updated. |  [optional]
**value** | [**BigDecimal**](BigDecimal.md) | Value of metric in selected config for reward definition |  [optional]
**valueType** | **String** | Type of config selected for reward definition |  [optional]


<a name="ExpirationModifierEnum"></a>
## Enum: ExpirationModifierEnum
Name | Value
---- | -----
STARTOFPERIOD | &quot;startOfPeriod&quot;
ENDOFPERIOD | &quot;endOfPeriod&quot;
NOMODIFICATION | &quot;noModification&quot;



