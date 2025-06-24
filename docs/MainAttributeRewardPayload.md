
# MainAttributeRewardPayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | [**BigDecimal**](BigDecimal.md) | Value of the selected reward config |  [optional]
**code** | **String** | Code generated to attribute reward to a contact |  [optional]
**contactId** | **Long** | Contact to attribute the reward |  [optional]
**expirationDate** | **String** | Reward expiration date |  [optional]
**loyaltySubscriptionId** | **String** | One of contactId or loyaltySubscriptionId is required |  [optional]
**meta** | **Map&lt;String, Object&gt;** | Offer meta information (key/value object) |  [optional]
**rewardId** | [**UUID**](UUID.md) | Reward id | 



