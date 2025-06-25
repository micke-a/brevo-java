
# GetCorporateInvitedUsersListFeatureAccess

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userManagement** | **List&lt;String&gt;** | User management accessiblity. |  [optional]
**apiKeys** | **List&lt;String&gt;** | Api keys accessiblity. |  [optional]
**myPlan** | **List&lt;String&gt;** | My plan accessiblity. |  [optional]
**appsManagement** | **List&lt;String&gt;** | Apps management accessiblity | Not available in ENTv2 |  [optional]
**subOrganizationGroups** | **List&lt;String&gt;** | Group creation, modification or deletion accessibility |  [optional]
**createSubOrganizations** | **List&lt;String&gt;** | Authorization to create sub-organization in the admin account. If the user creating the sub-organization, belongs to a group, the user must choose a group at the sub-organization creation. |  [optional]
**manageSubOrganizations** | **List&lt;String&gt;** | Authorization to manage and access sub-organizations in the admin account. |  [optional]
**analytics** | **List&lt;String&gt;** | Analytics dashboard accessibility |  [optional]
**security** | **List&lt;String&gt;** | Security page accessibility |  [optional]



