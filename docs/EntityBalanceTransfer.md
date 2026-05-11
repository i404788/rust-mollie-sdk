# EntityBalanceTransfer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a balance transfer object. Will always contain the string `connect-balance-transfer` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this balance transfer. Mollie assigns this identifier at balance transfer creation time. Mollie will always refer to the balance transfer by this ID. Example: `cbtr_j8NvRAM2WNZtsykpLEX8J`. | [readonly]
**amount** | [**models::Amount**](Amount.md) | The amount to be transferred, e.g. `{\"currency\":\"EUR\", \"value\":\"1000.00\"}` if you would like to transfer €1000.00. | 
**source** | [**models::EntityBalanceTransferParty**](EntityBalanceTransferParty.md) |  | 
**destination** | [**models::EntityBalanceTransferParty**](EntityBalanceTransferParty.md) |  | 
**description** | **String** | The transfer description for initiating party. | 
**status** | [**models::BalanceTransferStatus**](BalanceTransferStatus.md) |  | 
**status_reason** | [**models::EntityBalanceTransferStatusReason**](EntityBalanceTransferStatusReason.md) |  | 
**category** | Option<[**models::BalanceTransferCategory**](BalanceTransferCategory.md)> |  | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> | A JSON object that you can attach to a balance transfer. This can be useful for storing additional information about the transfer in a structured format. Maximum size is approximately 1KB. | [optional]
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**executed_at** | Option<**String**> | The date and time when the transfer was completed, in ISO 8601 format. This parameter is omitted if the transfer is not executed (yet). | [optional][readonly]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  You can enable test mode by setting `testmode` to `true`. | [optional]
**mode** | [**models::Mode**](Mode.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


