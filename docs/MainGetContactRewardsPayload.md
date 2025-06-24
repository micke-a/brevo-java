
# MainGetContactRewardsPayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contactId** | **Integer** | Contact to attribute the reward | 
**limit** | **Integer** | Number of documents per page |  [optional]
**metadata** | [**List&lt;MainFilter&gt;**](MainFilter.md) | Data to define the reward for that particular contact |  [optional]
**offset** | **Integer** | Index of the first document in the page |  [optional]
**rewardId** | **String** | Unique identifier of the associated reward |  [optional]
**sort** | [**SortEnum**](#SortEnum) | Sort the documents in the ascending or descending order |  [optional]
**sortField** | [**SortFieldEnum**](#SortFieldEnum) | Sort documents by field |  [optional]


<a name="SortEnum"></a>
## Enum: SortEnum
Name | Value
---- | -----
ASC | &quot;asc&quot;
DESC | &quot;desc&quot;


<a name="SortFieldEnum"></a>
## Enum: SortFieldEnum
Name | Value
---- | -----
UPDATEDAT | &quot;updatedAt&quot;
CREATEDAT | &quot;createdAt&quot;



