# UpdateSalesInvoiceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**testmode** | Option<**bool**> | Whether the entity was created in test mode or live mode. This field does not update the mode of the entity.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**status** | Option<[**models::SalesInvoiceStatusUpdate**](SalesInvoiceStatusUpdate.md)> | The status for the invoice to end up in.  Dependent parameters: `paymentDetails` for `paid`, `emailDetails` for `issued` and `paid`. | [optional]
**memo** | Option<**String**> | A free-form memo you can set on the invoice, and will be shown on the invoice PDF. | [optional]
**payment_term** | Option<[**models::SalesInvoicePaymentTerm**](SalesInvoicePaymentTerm.md)> |  | [optional]
**payment_details** | Option<[**models::SalesInvoicePaymentDetails**](SalesInvoicePaymentDetails.md)> | Used when setting an invoice to status of `paid`, and will store a payment that fully pays the invoice with the provided details. Required for `paid` status. | [optional]
**email_details** | Option<[**models::SalesInvoiceEmailDetails**](SalesInvoiceEmailDetails.md)> | Used when setting an invoice to status of either `issued` or `paid`. Will be used to issue the invoice to the recipient with the provided `subject` and `body`. Required for `issued` status. | [optional]
**recipient_identifier** | Option<**String**> | An identifier tied to the recipient data. This should be a unique value based on data your system contains, so that both you and us know who we're referring to. It is a value you provide to us so that recipient management is not required to send a first invoice to a recipient. | [optional]
**recipient** | Option<[**models::SalesInvoiceRecipient**](SalesInvoiceRecipient.md)> | The recipient object should contain all the information relevant to create an invoice for an intended recipient. This data will be stored, updated, and re-used as appropriate, based on the `recipientIdentifier`. | [optional]
**lines** | Option<[**Vec<models::SalesInvoiceLineItem>**](SalesInvoiceLineItem.md)> | Provide the line items for the invoice. Each line contains details such as a description of the item ordered and its price.  All lines must have the same currency as the invoice. | [optional]
**discount** | Option<[**models::SalesInvoiceDiscount**](SalesInvoiceDiscount.md)> | The discount to be applied to the entire invoice, possibly on top of the line item discounts. | [optional]
**is_e_invoice** | Option<**bool**> | This indicates whether the invoice is an e-invoice. The default value is `false` and can't be changed after the invoice has been issued.  When `emailDetails` is provided, an additional email is sent to the recipient. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


