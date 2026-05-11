# EntityInvoiceLinesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **String** | The administrative period in `YYYY-MM` on which the line should be booked. | 
**description** | **String** | Description of the product. | 
**count** | **i32** | Number of products invoiced. For example, the number of payments. | 
**vat_percentage** | **i32** | VAT percentage rate that applies to this product. | 
**amount** | [**models::Amount**](Amount.md) | Line item amount excluding VAT. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


