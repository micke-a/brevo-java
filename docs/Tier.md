
# Tier

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tierId** | [**UUID**](UUID.md) | Tier id |  [optional]
**name** | **String** | Tier name |  [optional]
**imageRef** | **String** | Tier image reference |  [optional]
**loyaltyProgramId** | [**UUID**](UUID.md) | Associated loyalty program Id |  [optional]
**groupId** | [**UUID**](UUID.md) | Associated group Id |  [optional]
**createdAt** | [**OffsetDateTime**] |  |  [optional]
**updatedAt** | [**OffsetDateTime**] |  |  [optional]
**accessConditions** | [**List&lt;TierAccessConditions&gt;**](TierAccessConditions.md) | Conditions required to access this tier |  [optional]
**tierRewards** | [**List&lt;TierTierRewards&gt;**](TierTierRewards.md) | Rewards associated with this tier |  [optional]



