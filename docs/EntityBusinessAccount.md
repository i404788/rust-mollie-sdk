# EntityBusinessAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a business account object. Will always contain the string `business-account` for this endpoint. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this business account. Mollie assigns this identifier at account creation time. | [optional][readonly]
**account_details** | Option<[**models::AccountDetails**](AccountDetails.md)> |  | [optional]
**balance** | Option<[**models::Balance**](Balance.md)> |  | [optional]
**status** | Option<[**models::AccountStatus**](AccountStatus.md)> |  | [optional]
**mode** | Option<[**models::Mode**](Mode.md)> |  | [optional]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


