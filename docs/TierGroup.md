
# TierGroup

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**UUID**](UUID.md) | Tier group unique identifier |  [optional]
**name** | **String** | Tier group name |  [optional]
**tierOrder** | [**List&lt;UUID&gt;**](UUID.md) | Order of the tiers in the group in ascending order |  [optional]
**loyaltyProgramId** | [**UUID**](UUID.md) | Associated loyalty program Id |  [optional]
**upgradeStrategy** | [**UpgradeStrategyEnum**](#UpgradeStrategyEnum) | Select real_time to upgrade tier on real time balance updates. Select membership_anniversary to upgrade tier on subscription anniversary. Select tier_anniversary to upgrade tier on tier anniversary. |  [optional]
**downgradeStrategy** | [**DowngradeStrategyEnum**](#DowngradeStrategyEnum) | Select real_time to downgrade tier on real time balance updates. Select membership_anniversary to downgrade tier on subscription anniversary. Select tier_anniversary to downgrade tier on tier anniversary. |  [optional]
**createdAt** | [**OffsetDateTime**] | Timestamp when the tier group was created |  [optional]
**updatedAt** | [**OffsetDateTime**] | Timestamp when the tier group was last updated |  [optional]


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



