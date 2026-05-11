# EntityCapability

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Always the word `capability` for this resource type. | 
**name** | **String** | A unique name for this capability like `payments` / `settlements`. | 
**status** | [**models::CapabilityStatus**](CapabilityStatus.md) |  | 
**status_reason** | Option<[**models::CapabilityStatusReason**](CapabilityStatusReason.md)> |  | 
**requirements** | [**Vec<models::EntityCapabilityRequirement>**](EntityCapabilityRequirement.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


