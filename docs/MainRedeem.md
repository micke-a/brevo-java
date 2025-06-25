
# MainRedeem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cancelledAt** | [**OffsetDateTime**] | Timestamp when the redemption was cancelled |  [optional]
**completedAt** | [**OffsetDateTime**] | Timestamp when the redemption was completed |  [optional]
**contactId** | **Long** | Unique identifier for the contact |  [optional]
**createdAt** | [**OffsetDateTime**] | Timestamp when the redemption was created |  [optional]
**debitTransactionId** | [**UUID**](UUID.md) | Unique identifier for the debit transaction |  [optional]
**expiresAt** | [**OffsetDateTime**] | Timestamp when the redemption expires |  [optional]
**id** | [**UUID**](UUID.md) | Unique identifier for the redemption |  [optional]
**loyaltyProgramId** | [**UUID**](UUID.md) | Unique identifier for the loyalty program |  [optional]
**meta** | **Map&lt;String, Object&gt;** | Additional metadata associated with the redemption |  [optional]
**rejectReason** | **String** | Reason for rejection if the redemption was rejected |  [optional]
**rejectedAt** | [**OffsetDateTime**] | Timestamp when the redemption was rejected |  [optional]
**rewardAttributionId** | [**UUID**](UUID.md) | Unique identifier for the reward attribution |  [optional]
**status** | **String** | Current status of the redemption |  [optional]
**updatedAt** | [**OffsetDateTime**] | Timestamp when the redemption was last updated |  [optional]



