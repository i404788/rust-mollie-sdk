# EntityBalanceTransaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a balance transaction object. Will always contain the string `balance-transaction` for this endpoint. | [optional][readonly]
**id** | Option<**String**> |  | [optional]
**r#type** | Option<[**models::BalanceTransactionType**](balance-transaction-type.md)> | The type of transaction, for example `payment` or `refund`. Values include the below examples, although this list is not definitive.  * Regular payment processing: `payment` `capture` `unauthorized-direct-debit` `failed-payment` * Refunds and chargebacks: `refund` `returned-refund` `chargeback` `chargeback-reversal` * Settlements: `outgoing-transfer` `canceled-outgoing-transfer` `returned-transfer` * Invoicing: `invoice-compensation` `balance-correction` * Mollie Connect: `application-fee` `split-payment` `platform-payment-refund` `platform-payment-chargeback` | [optional]
**result_amount** | Option<[**models::Amount**](amount.md)> | The final amount that was moved to or from the balance. If the transaction moves funds away from the balance, for example when it concerns a refund, the amount will be negative. | [optional]
**initial_amount** | Option<[**models::Amount**](amount.md)> | The amount that was to be moved to or from the balance, excluding deductions. If the transaction moves funds away from the balance, for example when it concerns a refund, the amount will be negative. | [optional]
**deductions** | Option<[**models::AmountNullable**](amount-nullable.md)> | The total amount of deductions withheld from the movement. For example, if we charge a €0.29 fee on a €10 payment, the deductions amount will be `{\"currency\":\"EUR\", \"value\":\"-0.29\"}`.  When moving funds to a balance, we always round the deduction to a 'real' amount. Any differences between these real-time rounded amounts and the final invoice will be compensated when the invoice is generated. | [optional]
**context** | Option<[**models::EntityBalanceTransactionContext**](entity_balance_transaction_context.md)> |  | [optional]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


