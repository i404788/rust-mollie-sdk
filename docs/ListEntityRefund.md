# ListEntityRefund

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a refund object. Will always contain the string `refund` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this refund. Mollie assigns this identifier at refund creation time. Mollie will always refer to the refund by this ID. Example: `re_4qqhO89gsT`. | [readonly]
**mode** | [**models::Mode**](Mode.md) |  | 
**description** | **String** | The description of the refund that may be shown to your customer, depending on the payment method used. | 
**amount** | [**models::Amount**](Amount.md) | The amount refunded to your customer with this refund. The amount is allowed to be lower than the original payment amount. | 
**settlement_amount** | Option<[**models::AmountNullable**](AmountNullable.md)> | **Deprecated.** This field will be removed on January 1st, 2027. Use the [Settlements API](list-settlements) or the [List balance transactions endpoint](list-balance-transactions) for settlement data.  The amount deducted from your account balance for this refund, converted to the currency your account is settled in. Always a **negative** amount. Only available once the refund is finalized and the final settlement amount has been determined.  For refunds not directly processed by Mollie (e.g. PayPal), the settlement amount is zero. | [optional][readonly]
**metadata** | Option<[**models::Metadata**](Metadata.md)> |  | 
**payment_id** | Option<**String**> | The unique identifier of the payment this refund was created for. The full payment object can be retrieved via the payment URL in the `_links` object. | [optional][readonly]
**settlement_id** | Option<**String**> | The identifier referring to the settlement this refund was settled with. This field is omitted if the refund is not settled (yet). | [optional][readonly]
**status** | [**models::RefundStatusResponse**](RefundStatusResponse.md) |  | [readonly]
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**external_reference** | Option<[**models::ListEntityRefundExternalReference**](ListEntityRefundExternalReference.md)> |  | [optional]
**reverse_routing** | Option<**bool**> | *This feature is only available to marketplace operators.*  With Mollie Connect you can charge fees on payments that your app is processing on behalf of other Mollie merchants, by providing the `routing` object during [payment creation](create-payment).  When creating refunds for these *routed* payments, by default the full amount is deducted from your balance.  If you want to pull back the funds that were routed to the connected merchant(s), you can set this parameter to `true` when issuing a full refund.  For more fine-grained control and for partial refunds, use the `routingReversals` parameter instead. | [optional]
**routing_reversals** | Option<[**Vec<models::ListEntityRefundRoutingReversalsInner>**](ListEntityRefundRoutingReversalsInner.md)> | *This feature is only available to marketplace operators.*  When creating refunds for *routed* payments, by default the full amount is deducted from your balance.  If you want to pull back funds from the connected merchant(s), you can use this parameter to specify what amount needs to be reversed from which merchant(s).  If you simply want to fully reverse the routed funds, you can also use the `reverseRouting` parameter instead. | [optional]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**_links** | [**models::ListEntityRefundLinks**](ListEntityRefundLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


