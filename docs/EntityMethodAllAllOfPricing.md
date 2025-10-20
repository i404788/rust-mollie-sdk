# EntityMethodAllAllOfPricing

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **String** | A description of what the pricing applies to. For example, a specific country (`The Netherlands`) or a category of cards (`American Express`). If a `locale` is provided, the description may be translated. | 
**fixed** | [**models::Amount**](amount.md) | The fixed price charged per payment. | 
**variable** | **String** | The variable price charged per payment, as a percentage string. | 
**fee_region** | Option<**String**> | Only present for credit card pricing. It will correspond with the `feeRegion` of credit card payments as returned in the [Payments API](get-payment). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


