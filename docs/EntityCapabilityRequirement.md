# EntityCapabilityRequirement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The name of this requirement, referring to the task to be fulfilled by the organization to enable or re-enable the capability. The name is unique among other requirements of the same capability. Examples include `needs-data` and `process-first-payment`. | 
**status** | [**models::CapabilityRequirementStatus**](CapabilityRequirementStatus.md) |  | 
**due_date** | Option<**String**> | Due date until the requirement must be fulfilled, if any. The date is shown in ISO-8601 format. | 
**_links** | [**models::EntityCapabilityRequirementLinks**](EntityCapabilityRequirementLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


