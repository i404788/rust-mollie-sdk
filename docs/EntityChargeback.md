# EntityChargeback

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a chargeback object. Will always contain the string `chargeback` for this endpoint. | [readonly]
**id** | **String** |  | 
**amount** | [**models::Amount**](amount.md) | The amount charged back by the customer. | 
**settlement_amount** | Option<[**models::AmountNullable**](amount-nullable.md)> | This optional field will contain the approximate amount that will be deducted from your account balance, converted to the currency your account is settled in.  The amount is a **negative** amount.  Since the field contains an estimated amount during chargeback processing, it may change over time. To retrieve accurate settlement amounts we recommend using the [List balance transactions endpoint](list-balance-transactions) instead. | [optional][readonly]
**reason** | Option<[**models::EntityChargebackReason**](entity_chargeback_reason.md)> |  | [optional]
**payment_id** | **String** |  | 
**settlement_id** | Option<**String**> |  | [optional]
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**reversed_at** | Option<**String**> | The date and time the chargeback was reversed if applicable, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | [**models::EntityRefundLinks**](entity_refund__links.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


