# EntityCapability

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Always the word `capability` for this resource type. | [optional]
**name** | Option<**String**> | A unique name for this capability like `payments` / `settlements`. | [optional]
**status** | Option<[**models::CapabilityStatus**](capability-status.md)> |  | [optional]
**status_reason** | Option<[**models::CapabilityStatusReason**](capability-status-reason.md)> |  | [optional]
**requirements** | Option<[**Vec<models::EntityCapabilityRequirement>**](entity-capability-requirement.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


