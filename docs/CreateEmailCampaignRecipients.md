
# CreateEmailCampaignRecipients

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**exclusionListIds** | **List&lt;Long&gt;** | List ids to exclude from the campaign |  [optional]
**listIds** | **List&lt;Long&gt;** | Mandatory if scheduledAt is not empty. List Ids to send the campaign to |  [optional]
**segmentIds** | **List&lt;Long&gt;** | Mandatory if listIds are not used. Segment ids to send the campaign to. |  [optional]
**exclusionSegmentIds** | **List&lt;Long&gt;** | Segment ids which have to be excluded from a campaign.  |  [optional]



