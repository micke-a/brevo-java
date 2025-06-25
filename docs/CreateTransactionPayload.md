
# CreateTransactionPayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**loyaltySubscriptionId** | **String** | Unique identifier for the loyalty subscription (required unless &#x60;contactId&#x60; is provided). |  [optional]
**amount** | [**BigDecimal**](BigDecimal.md) | Transaction amount (must be provided). | 
**autoComplete** | **Boolean** | Whether the transaction should be automatically completed. |  [optional]
**balanceDefinitionId** | **String** | Unique identifier (UUID) of the associated balance definition. | 
**balanceExpiryInMinutes** | **Integer** | Optional expiry time for the balance in minutes (must be greater than 0 if provided). |  [optional]
**contactId** | **Integer** | Unique identifier of the contact involved in the transaction (required unless &#x60;LoyaltySubscriptionId&#x60; is provided). |  [optional]
**eventTime** | **String** | Optional timestamp specifying when the transaction occurred. |  [optional]
**meta** | **Object** | Optional metadata associated with the transaction. |  [optional]
**ttl** | **Integer** | Optional time-to-live for the transaction (must be greater than 0 if provided). |  [optional]



