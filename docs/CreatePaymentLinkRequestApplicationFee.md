# CreatePaymentLinkRequestApplicationFee

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | [**models::Amount**](Amount.md) | The fee that you wish to charge.  Be careful to leave enough space for Mollie's own fees to be deducted as well. For example, you cannot charge a €0.99 fee on a €1.00 payment. | 
**description** | **String** | The description of the application fee. This will appear on settlement reports towards both you and the connected merchant. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


