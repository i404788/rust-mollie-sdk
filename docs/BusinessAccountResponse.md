# BusinessAccountResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a business account object. Will always contain the string `business-account` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this business account. Mollie assigns this identifier at account creation time. | [readonly]
**account_details** | [**models::AccountDetails**](AccountDetails.md) |  | 
**balance** | [**models::Balance**](Balance.md) |  | 
**status** | [**models::AccountStatus**](AccountStatus.md) |  | 
**mode** | [**models::Mode**](Mode.md) |  | 
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


