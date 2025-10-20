# EntitySalesInvoiceResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a sales invoice object. Will always contain the string `sales-invoice` for this endpoint. | [optional][readonly]
**id** | Option<**String**> |  | [optional]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**invoice_number** | Option<**String**> | When issued, an invoice number will be set for the sales invoice. | [optional][readonly]
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) this entity belongs to.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted in the creation request. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. | [optional]
**status** | Option<[**models::SalesInvoiceStatusResponse**](sales-invoice-status-response.md)> |  | [optional]
**vat_scheme** | Option<[**models::SalesInvoiceVatSchemeResponse**](sales-invoice-vat-scheme-response.md)> |  | [optional]
**vat_mode** | Option<[**models::SalesInvoiceVatModeResponse**](sales-invoice-vat-mode-response.md)> |  | [optional]
**memo** | Option<**String**> | A free-form memo you can set on the invoice, and will be shown on the invoice PDF. | [optional]
**metadata** | Option<[**serde_json::Value**](.md)> | Provide any data you like as a JSON object. We will save the data alongside the entity. Whenever you fetch the entity with our API, we will also include the metadata. You can use up to approximately 1kB. | [optional]
**payment_term** | Option<[**models::SalesInvoicePaymentTermResponse**](sales-invoice-payment-term-response.md)> |  | [optional]
**payment_details** | Option<[**models::SalesInvoicePaymentDetailsResponse**](sales-invoice-payment-details-response.md)> | Used when setting an invoice to status of `paid`, and will store a payment that fully pays the invoice with the provided details. Required for `paid` status. | [optional]
**email_details** | Option<[**models::SalesInvoiceEmailDetails**](sales-invoice-email-details.md)> | Used when setting an invoice to status of either `issued` or `paid`. Will be used to issue the invoice to the recipient with the provided `subject` and `body`. Required for `issued` status. | [optional]
**customer_id** | Option<**String**> | The identifier referring to the [customer](get-customer) you want to attempt an automated payment for. If provided, `mandateId` becomes required as well. Only allowed for invoices with status `paid`. | [optional]
**mandate_id** | Option<**String**> | The identifier referring to the [mandate](get-mandate) you want to use for the automated payment. If provided, `customerId` becomes required as well. Only allowed for invoices with status `paid`. | [optional]
**recipient_identifier** | Option<**String**> | An identifier tied to the recipient data. This should be a unique value based on data your system contains, so that both you and us know who we're referring to. It is a value you provide to us so that recipient management is not required to send a first invoice to a recipient. | [optional]
**recipient** | Option<[**models::SalesInvoiceRecipientResponse**](sales-invoice-recipient-response.md)> |  | [optional]
**lines** | Option<[**Vec<models::SalesInvoiceLineItemResponse>**](sales-invoice-line-item-response.md)> | Provide the line items for the invoice. Each line contains details such as a description of the item ordered and its price.  All lines must have the same currency as the invoice. | [optional]
**discount** | Option<[**models::SalesInvoiceDiscountResponse**](sales-invoice-discount-response.md)> | The discount to be applied to the entire invoice, applied on top of any line item discounts. | [optional]
**amount_due** | Option<[**models::Amount**](amount.md)> | The amount that is left to be paid. | [optional][readonly]
**subtotal_amount** | Option<[**models::Amount**](amount.md)> | The total amount without VAT before discounts. | [optional][readonly]
**total_amount** | Option<[**models::Amount**](amount.md)> | The total amount with VAT. | [optional][readonly]
**total_vat_amount** | Option<[**models::Amount**](amount.md)> | The total VAT amount. | [optional][readonly]
**discounted_subtotal_amount** | Option<[**models::Amount**](amount.md)> | The total amount without VAT after discounts. | [optional][readonly]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**issued_at** | Option<**String**> | If issued, the date when the sales invoice was issued, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**paid_at** | Option<**String**> | If paid, the date when the sales invoice was paid, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**due_at** | Option<**String**> | If issued, the date when the sales invoice payment is due, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | Option<[**models::EntitySalesInvoiceLinks**](entity_sales_invoice__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


