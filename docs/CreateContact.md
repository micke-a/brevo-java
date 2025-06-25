
# CreateContact

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **String** | Email address of the user. **Mandatory if &quot;ext_id&quot;  &amp; &quot;SMS&quot; field is not passed.** |  [optional]
**extId** | **String** | Pass your own Id to create a contact. |  [optional]
**attributes** | **Map&lt;String, Object&gt;** | Pass the set of attributes and their values. These attributes must be present in your Brevo account. For eg. {&#39;FNAME&#39;:&#39;Elly&#39;, &#39;LNAME&#39;:&#39;Roger&#39;, &#39;COUNTRIES&#39;:[&#39;India&#39;,&#39;China&#39;]} |  [optional]
**emailBlacklisted** | **Boolean** | Set this field to blacklist the contact for emails (emailBlacklisted &#x3D; true) |  [optional]
**smsBlacklisted** | **Boolean** | Set this field to blacklist the contact for SMS (smsBlacklisted &#x3D; true) |  [optional]
**listIds** | **List&lt;Long&gt;** | Ids of the lists to add the contact to |  [optional]
**updateEnabled** | **Boolean** | Facilitate to update the existing contact in the same request (updateEnabled &#x3D; true) |  [optional]
**smtpBlacklistSender** | **List&lt;String&gt;** | transactional email forbidden sender for contact. Use only for email Contact ( only available if updateEnabled &#x3D; true ) |  [optional]



