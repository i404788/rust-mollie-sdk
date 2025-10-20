# EntityRefundResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a refund object. Will always contain the string `refund` for this endpoint. | [readonly]
**id** | **String** |  | 
**mode** | [**models::Mode**](mode.md) |  | 
**description** | **String** | The description of the refund that may be shown to your customer, depending on the payment method used. | 
**amount** | [**models::Amount**](amount.md) | The amount refunded to your customer with this refund. The amount is allowed to be lower than the original payment amount. | 
**settlement_amount** | Option<[**models::AmountNullable**](amount-nullable.md)> | This optional field will contain the approximate amount that will be deducted from your account balance, converted to the currency your account is settled in.  The amount is a **negative** amount.  If the refund is not directly processed by Mollie, for example for PayPal refunds, the settlement amount will be zero.  Since the field contains an estimated amount during refund processing, it may change over time. For example, while the refund is queued the settlement amount is likely not yet available.  To retrieve accurate settlement amounts we recommend using the [List balance transactions endpoint](list-balance-transactions) instead. | [optional][readonly]
**metadata** | Option<[**models::Metadata**](metadata.md)> |  | 
**payment_id** | Option<**String**> |  | [optional]
**settlement_id** | Option<**String**> |  | [optional]
**status** | [**models::RefundStatus**](refund-status.md) |  | [readonly]
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**external_reference** | Option<[**models::EntityRefundResponseExternalReference**](entity_refund_response_externalReference.md)> |  | [optional]
**reverse_routing** | Option<**bool**> | *This feature is only available to marketplace operators.*  With Mollie Connect you can charge fees on payments that your app is processing on behalf of other Mollie merchants, by providing the `routing` object during [payment creation](create-payment).  When creating refunds for these *routed* payments, by default the full amount is deducted from your balance.  If you want to pull back the funds that were routed to the connected merchant(s), you can set this parameter to `true` when issuing a full refund.  For more fine-grained control and for partial refunds, use the `routingReversals` parameter instead. | [optional]
**routing_reversals** | Option<[**Vec<models::EntityRefundRoutingReversalsInner>**](entity_refund_routingReversals_inner.md)> | *This feature is only available to marketplace operators.*  When creating refunds for *routed* payments, by default the full amount is deducted from your balance.  If you want to pull back funds from the connected merchant(s), you can use this parameter to specify what amount needs to be reversed from which merchant(s).  If you simply want to fully reverse the routed funds, you can also use the `reverseRouting` parameter instead. | [optional]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**_links** | [**models::EntityRefundLinks**](entity_refund__links.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


