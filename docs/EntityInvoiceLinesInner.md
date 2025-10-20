# EntityInvoiceLinesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | Option<**String**> | The administrative period in `YYYY-MM` on which the line should be booked. | [optional]
**description** | Option<**String**> | Description of the product. | [optional]
**count** | Option<**i32**> | Number of products invoiced. For example, the number of payments. | [optional]
**vat_percentage** | Option<**i32**> | VAT percentage rate that applies to this product. | [optional]
**amount** | Option<[**models::Amount**](amount.md)> | Line item amount excluding VAT. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


