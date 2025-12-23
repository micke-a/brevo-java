
# RequestContactExport

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**exportAttributes** | **List&lt;String&gt;** | List of all the attributes that you want to export. These attributes must be present in your contact database. It is required if exportMandatoryAttributes is set false. For example, [&#39;fname&#39;, &#39;lname&#39;, &#39;email&#39;]. |  [optional]
**customContactFilter** | [**RequestContactExportCustomContactFilter**](RequestContactExportCustomContactFilter.md) |  | 
**notifyUrl** | **String** | Webhook that will be called once the export process is finished. For reference, https://help.brevo.com/hc/en-us/articles/360007666479 |  [optional]
**disableNotification** | **Boolean** | To avoid generating the email notification upon contact export, pass **true** |  [optional]
**exportMandatoryAttributes** | **Boolean** | To export mandatory attributes like EMAIL, ADDED_TIME, MODIFIED_TIME |  [optional]
**exportSubscriptionStatus** | **List&lt;String&gt;** | Export subscription status of contacts for email &amp; sms marketting. Pass email_marketing to obtain the marketing email subscription status &amp; sms_marketing to retrieve the marketing SMS status of the contact. |  [optional]
**exportMetadata** | **List&lt;String&gt;** | Export metadata of contacts such as _listIds, ADDED_TIME, MODIFIED_TIME. |  [optional]
**exportDateInUTC** | **Boolean** | Specifies whether the date fields createdAt, modifiedAt in the exported data should be returned in UTC format. |  [optional]



