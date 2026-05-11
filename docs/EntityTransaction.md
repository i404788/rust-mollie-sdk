# EntityTransaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a business account transaction object. Will always contain the string `business-account-transaction` for this endpoint. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this transaction. Mollie assigns this identifier at transaction creation time. | [optional][readonly]
**business_account_id** | Option<**String**> | The identifier of the business account this transaction belongs to. | [optional][readonly]
**credit_debit_indicator** | Option<[**models::CreditDebitIndicator**](CreditDebitIndicator.md)> |  | [optional]
**r#type** | Option<[**models::TransactionType**](TransactionType.md)> |  | [optional]
**amount** | Option<[**models::Amount**](Amount.md)> | The amount of the transaction, e.g. `{\"currency\":\"EUR\", \"value\":\"100.00\"}`. | [optional]
**description** | Option<**String**> | A short description of the transaction. | [optional]
**counterparty** | Option<[**models::Counterparty**](Counterparty.md)> | The counterparty involved in this transaction. | [optional]
**after_balance** | Option<[**models::AfterBalance**](AfterBalance.md)> | The balance of the business account after this transaction was processed. | [optional]
**processed_at** | Option<**String**> | The date and time when the transaction was processed, in ISO 8601 format. | [optional][readonly]
**mode** | Option<[**models::Mode**](Mode.md)> |  | [optional]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


