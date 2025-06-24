
# AddContactToList

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emails** | **List&lt;String&gt;** | Mandatory if IDs, EXT_ID attributes are not passed, ignored otherwise. Emails to add to a list. You can pass a maximum of 150 emails for addition in one request. If you need to add the emails in bulk, please prefer /contacts/import api. |  [optional]
**ids** | **List&lt;Long&gt;** | Mandatory if Emails, EXT_ID attributes are not passed, ignored otherwise. Emails to add to a list. You can pass a maximum of 150 ids for addition in one request. If you need to add the emails in bulk, please prefer /contacts/import api. |  [optional]
**extIds** | **List&lt;String&gt;** | Mandatory if Emails, IDs are not passed, ignored otherwise. Emails to add to a list. You can pass a maximum of 150 extIds for addition in one request. If you need to add the emails in bulk, please prefer /contacts/import api. |  [optional]



