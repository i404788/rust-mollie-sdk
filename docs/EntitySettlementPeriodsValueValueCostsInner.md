# EntitySettlementPeriodsValueValueCostsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **String** | A description of the cost subtotal | 
**method** | Option<[**models::PaymentMethod**](PaymentMethod.md)> |  | 
**count** | **i32** | The number of fees | 
**rate** | [**models::EntitySettlementPeriodsValueValueCostsInnerRate**](EntitySettlementPeriodsValueValueCostsInnerRate.md) |  | 
**amount_net** | [**models::Amount**](Amount.md) | The net total cost, i.e. excluding VAT | 
**amount_vat** | [**models::AmountNullable**](AmountNullable.md) | The applicable VAT | 
**amount_gross** | [**models::Amount**](Amount.md) | The gross total cost, i.e. including VAT | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


