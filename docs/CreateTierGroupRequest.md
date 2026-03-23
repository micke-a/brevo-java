
# CreateTierGroupRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Name of the tier group | 
**upgradeStrategy** | [**UpgradeStrategyEnum**](#UpgradeStrategyEnum) | Select real_time to upgrade tier on real time balance updates. Select membership_anniversary to upgrade tier on subscription anniversary. Select tier_anniversary to upgrade tier on tier anniversary. |  [optional]
**downgradeStrategy** | [**DowngradeStrategyEnum**](#DowngradeStrategyEnum) | Select real_time to downgrade tier on real time balance updates. Select membership_anniversary to downgrade tier on subscription anniversary. Select tier_anniversary to downgrade tier on tier anniversary. |  [optional]
**tierOrder** | **List&lt;String&gt;** | Order of the tiers in the group in ascending order |  [optional]
**meta** | **Map&lt;String, Object&gt;** | Additional metadata for the tier group |  [optional]


<a name="UpgradeStrategyEnum"></a>
## Enum: UpgradeStrategyEnum
Name | Value
---- | -----
REAL_TIME | &quot;real_time&quot;
MEMBERSHIP_ANNIVERSARY | &quot;membership_anniversary&quot;
TIER_ANNIVERSARY | &quot;tier_anniversary&quot;


<a name="DowngradeStrategyEnum"></a>
## Enum: DowngradeStrategyEnum
Name | Value
---- | -----
REAL_TIME | &quot;real_time&quot;
MEMBERSHIP_ANNIVERSARY | &quot;membership_anniversary&quot;
TIER_ANNIVERSARY | &quot;tier_anniversary&quot;



