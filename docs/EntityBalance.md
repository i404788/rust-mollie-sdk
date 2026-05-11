# EntityBalance

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a balance object. Will always contain the string `balance` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this balance. | [readonly]
**mode** | [**models::Mode**](Mode.md) |  | 
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**currency** | [**models::Currencies**](Currencies.md) | The balance's ISO 4217 currency code. | [readonly]
**description** | **String** | The description or name of the balance. Can be used to denote the purpose of the balance. | [readonly]
**status** | [**models::BalanceStatus**](BalanceStatus.md) |  | [readonly]
**transfer_frequency** | Option<[**models::BalanceTransferFrequency**](BalanceTransferFrequency.md)> |  | [optional][readonly]
**transfer_threshold** | Option<[**models::Amount**](Amount.md)> | The minimum amount configured for scheduled automatic settlements. As soon as the amount on the balance exceeds this threshold, the complete balance will be paid out to the transfer destination according to the configured frequency. | [optional][readonly]
**transfer_reference** | Option<**String**> | The transfer reference set to be included in all the transfers for this balance. | [optional][readonly]
**transfer_destination** | Option<[**models::EntityBalanceTransferDestination**](EntityBalanceTransferDestination.md)> |  | [optional]
**available_amount** | [**models::Amount**](Amount.md) | The amount directly available on the balance, e.g. `{\"currency\":\"EUR\", \"value\":\"100.00\"}`. | [readonly]
**pending_amount** | [**models::Amount**](Amount.md) | The total amount that is queued to be transferred to your balance. For example, a credit card payment can take a few days to clear. | [readonly]
**_links** | [**models::EntityBalanceLinks**](EntityBalanceLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


