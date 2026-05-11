# SalesInvoiceLineItemResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **String** | A description of the line item. For example *LEGO 4440 Forest Police Station*. | 
**quantity** | **i32** | The number of items. | 
**vat_rate** | **String** | The vat rate to be applied to this line item. | 
**unit_price** | [**models::Amount**](Amount.md) | The price of a single item excluding VAT.  For example: `{\"currency\":\"EUR\", \"value\":\"89.00\"}` if the box of LEGO costs €89.00 each.  The unit price can be zero in case of free items. | 
**discount** | Option<[**models::SalesInvoiceDiscountResponse**](SalesInvoiceDiscountResponse.md)> | The discount to be applied to the line item. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


