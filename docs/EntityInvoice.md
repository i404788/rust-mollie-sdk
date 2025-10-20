# EntityInvoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates that the response contains an invoice object. Will always contain the string `invoice` for this endpoint. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this invoice. Example: `inv_FrvewDA3Pr`. | [optional][readonly]
**reference** | Option<**String**> | The reference number of the invoice. An example value would be: `2024.10000`. | [optional][readonly]
**vat_number** | Option<**String**> | The VAT number to which the invoice was issued to, if applicable. | [optional][readonly]
**status** | Option<[**models::InvoiceStatus**](invoice-status.md)> |  | [optional][readonly]
**net_amount** | Option<[**models::Amount**](amount.md)> | Total amount of the invoice, excluding VAT. | [optional][readonly]
**vat_amount** | Option<[**models::Amount**](amount.md)> | VAT amount of the invoice. Only applicable to merchants registered in the Netherlands. For EU merchants, VAT will be shifted to the recipient (as per article 44 and 196 in the EU VAT Directive 2006/112). For merchants outside the EU, no VAT will be charged. | [optional][readonly]
**gross_amount** | Option<[**models::Amount**](amount.md)> | Total amount of the invoice, including VAT. | [optional][readonly]
**lines** | Option<[**Vec<models::EntityInvoiceLinesInner>**](entity_invoice_lines_inner.md)> | The collection of products which make up the invoice. | [optional]
**issued_at** | Option<**String**> | The invoice date in `YYYY-MM-DD` format. | [optional][readonly]
**paid_at** | Option<**String**> | The date on which the invoice was paid, if applicable, in `YYYY-MM-DD` format. | [optional][readonly]
**due_at** | Option<**String**> | The date on which the invoice is due, if applicable, in `YYYY-MM-DD` format. | [optional][readonly]
**_links** | Option<[**models::EntityInvoiceLinks**](entity_invoice__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


