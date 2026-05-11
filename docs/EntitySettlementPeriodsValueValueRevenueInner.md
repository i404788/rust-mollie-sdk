# EntitySettlementPeriodsValueValueRevenueInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **String** | A description of the revenue subtotal | 
**method** | Option<[**models::PaymentMethod**](PaymentMethod.md)> |  | 
**count** | **i32** | The number of payments | 
**amount_net** | [**models::Amount**](Amount.md) | The net total of received funds, i.e. excluding VAT | 
**amount_vat** | [**models::AmountNullable**](AmountNullable.md) | The applicable VAT | 
**amount_gross** | [**models::Amount**](Amount.md) | The gross total of received funds, i.e. including VAT | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


