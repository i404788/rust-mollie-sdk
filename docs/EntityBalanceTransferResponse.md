# EntityBalanceTransferResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a balance transfer object. Will always contain the string `connect-balance-transfer` for this endpoint. | [readonly]
**id** | **String** |  | 
**amount** | [**models::Amount**](amount.md) | The amount to be transferred, e.g. `{\"currency\":\"EUR\", \"value\":\"1000.00\"}` if you would like to transfer €1000.00. | 
**source** | [**models::EntityBalanceTransferPartyResponse**](entity-balance-transfer-party-response.md) |  | 
**destination** | [**models::EntityBalanceTransferPartyResponse**](entity-balance-transfer-party-response.md) |  | 
**description** | **String** | The transfer description for initiating party. | 
**status** | [**models::BalanceTransferStatus**](balance-transfer-status.md) |  | 
**status_reason** | [**models::EntityBalanceTransferResponseStatusReason**](entity_balance_transfer_response_statusReason.md) |  | 
**category** | Option<[**models::BalanceTransferCategoryResponse**](balance-transfer-category-response.md)> |  | [optional]
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**executed_at** | Option<**String**> | The date and time when the transfer was completed, in ISO 8601 format. This parameter is omitted if the transfer is not executed (yet). | [optional][readonly]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**mode** | [**models::Mode**](mode.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


