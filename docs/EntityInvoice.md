# EntityInvoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates that the response contains an invoice object. Will always contain the string `invoice` for this endpoint. | [readonly]
**id** | **String** |  | [readonly]
**reference** | **String** | The reference number of the invoice. An example value would be: `2024.10000`. | [readonly]
**vat_number** | Option<**String**> | The VAT number to which the invoice was issued to, if applicable. | [readonly]
**status** | [**models::InvoiceStatus**](InvoiceStatus.md) |  | [readonly]
**net_amount** | [**models::Amount**](Amount.md) | Total amount of the invoice, excluding VAT. | [readonly]
**vat_amount** | [**models::Amount**](Amount.md) | VAT amount of the invoice. Only applicable to merchants registered in the Netherlands. For EU merchants, VAT will be shifted to the recipient (as per article 44 and 196 in the EU VAT Directive 2006/112). For merchants outside the EU, no VAT will be charged. | [readonly]
**gross_amount** | [**models::Amount**](Amount.md) | Total amount of the invoice, including VAT. | [readonly]
**lines** | [**Vec<models::EntityInvoiceLinesInner>**](EntityInvoiceLinesInner.md) | The collection of products which make up the invoice. | [readonly]
**issued_at** | **String** | The invoice date in `YYYY-MM-DD` format. | [readonly]
**paid_at** | Option<**String**> | The date on which the invoice was paid, if applicable, in `YYYY-MM-DD` format. | [optional][readonly]
**due_at** | Option<**String**> | The date on which the invoice is due, if applicable, in `YYYY-MM-DD` format. | [optional][readonly]
**_links** | [**models::EntityInvoiceLinks**](EntityInvoiceLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


