
# SendSmtpEmailMessageVersions

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to** | [**List&lt;SendSmtpEmailTo1&gt;**](SendSmtpEmailTo1.md) | List of email addresses and names (_optional_) of the recipients. For example, [{&quot;name&quot;:&quot;Jimmy&quot;, &quot;email&quot;:&quot;jimmy98@example.com&quot;}, {&quot;name&quot;:&quot;Joe&quot;, &quot;email&quot;:&quot;joe@example.com&quot;}] | 
**params** | **Map&lt;String, Object&gt;** | Pass the set of attributes to customize the template. For example, {&quot;FNAME&quot;:&quot;Joe&quot;, &quot;LNAME&quot;:&quot;Doe&quot;}. It&#39;s considered only if template is in New Template Language format. |  [optional]
**bcc** | [**List&lt;SendSmtpEmailBcc&gt;**](SendSmtpEmailBcc.md) | List of email addresses and names (optional) of the recipients in bcc |  [optional]
**cc** | [**List&lt;SendSmtpEmailCc&gt;**](SendSmtpEmailCc.md) | List of email addresses and names (optional) of the recipients in cc |  [optional]
**replyTo** | [**SendSmtpEmailReplyTo1**](SendSmtpEmailReplyTo1.md) |  |  [optional]
**subject** | **String** | Custom subject specific to message version  |  [optional]
**htmlContent** | **String** | HTML body of the message. **Mandatory if &#39;templateId&#39; is not passed, ignored if &#39;templateId&#39; is passed**  |  [optional]
**textContent** | **String** | Plain Text body of the message. **Ignored if &#39;templateId&#39; is passed**  |  [optional]
**headers** | **Object** | Pass the set of custom headers (not the standard headers) that shall be sent along the mail headers in the original email. &#39;sender.ip&#39; header can be set (only for dedicated ip users) to mention the IP to be used for sending transactional emails. Headers are allowed in &#x60;This-Case-Only&#x60; (i.e. words separated by hyphen with first letter of each word in capital letter), they will be converted to such case styling if not in this format in the request payload. For example, &#x60;{&quot;sender.ip&quot;:&quot;1.2.3.4&quot;, &quot;X-Mailin-custom&quot;:&quot;some_custom_header&quot;, &quot;idempotencyKey&quot;:&quot;abc-123&quot;}&#x60;. |  [optional]



