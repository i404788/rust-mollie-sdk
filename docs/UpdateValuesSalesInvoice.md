# UpdateValuesSalesInvoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. | [optional]
**status** | Option<[**models::SalesInvoiceStatus**](sales-invoice-status.md)> | The status for the invoice to end up in.  Dependent parameters: `paymentDetails` for `paid`, `emailDetails` for `issued` and `paid`. | [optional]
**memo** | Option<**String**> | A free-form memo you can set on the invoice, and will be shown on the invoice PDF. | [optional]
**payment_term** | Option<[**models::SalesInvoicePaymentTerm**](sales-invoice-payment-term.md)> |  | [optional]
**payment_details** | Option<[**models::SalesInvoicePaymentDetails**](sales-invoice-payment-details.md)> | Used when setting an invoice to status of `paid`, and will store a payment that fully pays the invoice with the provided details. Required for `paid` status. | [optional]
**email_details** | Option<[**models::SalesInvoiceEmailDetails**](sales-invoice-email-details.md)> | Used when setting an invoice to status of either `issued` or `paid`. Will be used to issue the invoice to the recipient with the provided `subject` and `body`. Required for `issued` status. | [optional]
**recipient_identifier** | Option<**String**> | An identifier tied to the recipient data. This should be a unique value based on data your system contains, so that both you and us know who we're referring to. It is a value you provide to us so that recipient management is not required to send a first invoice to a recipient. | [optional]
**recipient** | Option<[**models::SalesInvoiceRecipient**](sales-invoice-recipient.md)> | The recipient object should contain all the information relevant to create an invoice for an intended recipient. This data will be stored, updated, and re-used as appropriate, based on the `recipientIdentifier`. | [optional]
**lines** | Option<[**Vec<models::SalesInvoiceLineItem>**](sales-invoice-line-item.md)> | Provide the line items for the invoice. Each line contains details such as a description of the item ordered and its price.  All lines must have the same currency as the invoice. | [optional]
**discount** | Option<[**models::SalesInvoiceDiscount**](sales-invoice-discount.md)> | The discount to be applied to the entire invoice, possibly on top of the line item discounts. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


