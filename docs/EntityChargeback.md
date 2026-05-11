# EntityChargeback

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a chargeback object. Will always contain the string `chargeback` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this chargeback. Example: `chb_n9z0tp`. | [readonly]
**amount** | [**models::Amount**](Amount.md) | The amount charged back by the customer. | 
**settlement_amount** | Option<[**models::AmountNullable**](AmountNullable.md)> | **Deprecated.** This field will be removed on January 1st, 2027. Use the [Settlements API](list-settlements) or the [List balance transactions endpoint](list-balance-transactions) for settlement data.  The amount deducted from your account balance for this chargeback, converted to the currency your account is settled in. Always a **negative** amount. Only available once the chargeback is finalized and the final settlement amount has been determined. | [optional][readonly]
**reason** | Option<[**models::EntityChargebackReason**](EntityChargebackReason.md)> |  | [optional]
**payment_id** | **String** | The unique identifier of the payment this chargeback was created for. For example: `tr_5B8cwPMGnU6qLbRvo7qEZo`. The full payment object can be retrieved via the payment URL in the `_links` object. | [readonly]
**settlement_id** | Option<**String**> | The identifier referring to the settlement this payment was settled with. For example, `stl_BkEjN2eBb`. This field is omitted if the refund is not settled (yet). | [optional][readonly]
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**reversed_at** | Option<**String**> | The date and time the chargeback was reversed if applicable, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | [**models::EntityChargebackLinks**](EntityChargebackLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


