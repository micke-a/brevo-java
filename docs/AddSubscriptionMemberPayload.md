
# AddSubscriptionMemberPayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contactId** | **Integer** | Required if LoyaltySubscriptionId is not provided, must be greater than 0 |  [optional]
**loyaltySubscriptionId** | **String** | Required if ContactId is not provided, max length 64 |  [optional]
**memberContactIds** | **List&lt;Integer&gt;** | Required, each item must be greater than or equal to 1 | 



