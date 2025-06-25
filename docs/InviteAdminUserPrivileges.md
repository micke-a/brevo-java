
# InviteAdminUserPrivileges

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**feature** | [**FeatureEnum**](#FeatureEnum) | Feature name |  [optional]
**permissions** | [**List&lt;PermissionsEnum&gt;**](#List&lt;PermissionsEnum&gt;) | Permissions for a given feature |  [optional]


<a name="FeatureEnum"></a>
## Enum: FeatureEnum
Name | Value
---- | -----
MY_PLAN | &quot;my_plan&quot;
API | &quot;api&quot;
USER_MANAGEMENT | &quot;user_management&quot;
APP_MANAGEMENT | &quot;app_management&quot;
SUB_ORGANIZATION_GROUPS | &quot;sub_organization_groups&quot;
CREATE_SUB_ORGANIZATIONS | &quot;create_sub_organizations&quot;
MANAGE_SUB_ORGANIZATIONS | &quot;manage_sub_organizations&quot;
ANALYTICS | &quot;analytics&quot;
SECURITY | &quot;security&quot;


<a name="List<PermissionsEnum>"></a>
## Enum: List&lt;PermissionsEnum&gt;
Name | Value
---- | -----
ALL | &quot;all&quot;
NONE | &quot;none&quot;
CREATE | &quot;create&quot;
EDIT_DELETE | &quot;edit_delete&quot;
DOWNLOAD_DATA | &quot;download_data&quot;
CREATE_ALERTS | &quot;create_alerts&quot;



