# EntityBalance

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a balance object. Will always contain the string `balance` for this endpoint. | [optional][readonly]
**id** | Option<**String**> |  | [optional]
**mode** | Option<[**models::Mode**](mode.md)> |  | [optional]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**currency** | Option<[**models::Currencies**](currencies.md)> | The balance's ISO 4217 currency code. | [optional][readonly]
**description** | Option<**String**> | The description or name of the balance. Can be used to denote the purpose of the balance. | [optional][readonly]
**status** | Option<[**models::BalanceStatus**](balance-status.md)> |  | [optional][readonly]
**transfer_frequency** | Option<[**models::BalanceTransferFrequency**](balance-transfer-frequency.md)> |  | [optional][readonly]
**transfer_threshold** | Option<[**models::Amount**](amount.md)> | The minimum amount configured for scheduled automatic settlements. As soon as the amount on the balance exceeds this threshold, the complete balance will be paid out to the transfer destination according to the configured frequency. | [optional][readonly]
**transfer_reference** | Option<**String**> | The transfer reference set to be included in all the transfers for this balance. | [optional][readonly]
**transfer_destination** | Option<[**models::EntityBalanceTransferDestination**](entity_balance_transferDestination.md)> |  | [optional]
**available_amount** | Option<[**models::Amount**](amount.md)> | The amount directly available on the balance, e.g. `{\"currency\":\"EUR\", \"value\":\"100.00\"}`. | [optional][readonly]
**pending_amount** | Option<[**models::Amount**](amount.md)> | The total amount that is queued to be transferred to your balance. For example, a credit card payment can take a few days to clear. | [optional][readonly]
**_links** | Option<[**models::EntityBalanceLinks**](entity_balance__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


