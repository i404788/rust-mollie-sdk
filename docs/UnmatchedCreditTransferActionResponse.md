# UnmatchedCreditTransferActionResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | The resource type of the object. | [readonly]
**id** | **String** | The identifier uniquely referring to this unmatched credit transfer action. | [readonly]
**unmatched_credit_transfer_id** | **String** | The identifier of the unmatched credit transfer this action belongs to. | [readonly]
**action** | [**models::UnmatchedCreditTransferActionType**](UnmatchedCreditTransferActionType.md) | The action performed on the unmatched credit transfer. | [readonly]
**status** | [**models::UnmatchedCreditTransferActionStatus**](UnmatchedCreditTransferActionStatus.md) | The current status of the action. | [readonly]
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**details** | Option<[**models::EntityUnmatchedCreditTransferActionDetails**](EntityUnmatchedCreditTransferActionDetails.md)> |  | [optional]
**_links** | [**models::EntityUnmatchedCreditTransferActionLinks**](EntityUnmatchedCreditTransferActionLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


