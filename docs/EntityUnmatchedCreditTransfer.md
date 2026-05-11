# EntityUnmatchedCreditTransfer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains an unmatched credit transfer object. Will always contain the string `unmatched-credit-transfer` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this unmatched credit transfer. | [readonly]
**profile_id** | **String** | The identifier referring to the [profile](get-profile) this entity belongs to.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted in the creation request. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. | [readonly]
**amount** | [**models::Amount**](Amount.md) |  | 
**source** | [**models::EntityUnmatchedCreditTransferSource**](EntityUnmatchedCreditTransferSource.md) |  | 
**remittance_information** | [**models::EntityUnmatchedCreditTransferRemittanceInformation**](EntityUnmatchedCreditTransferRemittanceInformation.md) |  | 
**status** | [**models::UnmatchedCreditTransferStatus**](UnmatchedCreditTransferStatus.md) | The status of the unmatched credit transfer. | 
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**expires_at** | **String** | The date and time at which the unmatched credit transfer expires, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**payment_ids** | Option<**Vec<String>**> | The IDs of the payments this credit transfer was matched to. Only present when the status is `matched`. | [optional][readonly]
**_links** | [**models::EntityUnmatchedCreditTransferLinks**](EntityUnmatchedCreditTransferLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


