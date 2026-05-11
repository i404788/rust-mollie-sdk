# SalesInvoiceRecipientResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | [**models::SalesInvoiceRecipientTypeResponse**](SalesInvoiceRecipientTypeResponse.md) |  | 
**title** | Option<**String**> | The title of the `consumer` type recipient, for example Mr. or Mrs.. | [optional]
**given_name** | Option<**String**> | The given name (first name) of the `consumer` type recipient should be at least two characters and cannot contain only numbers. | [optional]
**family_name** | Option<**String**> | The given name (last name) of the `consumer` type recipient should be at least two characters and cannot contain only numbers. | [optional]
**organization_name** | Option<**String**> | The trading name of the `business` type recipient. | [optional]
**organization_number** | Option<**String**> | The Chamber of Commerce number of the organization for a `business` type recipient. Either this or `vatNumber` has to be provided. | [optional]
**vat_number** | Option<**String**> | The VAT number of the organization for a `business` type recipient. Either this or `organizationNumber` has to be provided. | [optional]
**email** | **String** | The email address of the recipient.  If the domain contains non-ASCII characters, encode it as Punycode per [RFC 3492](https://www.rfc-editor.org/rfc/rfc3492). | 
**phone** | Option<**String**> | The phone number of the recipient. | [optional]
**street_and_number** | **String** | A street and street number. | 
**street_additional** | Option<**String**> | Any additional addressing details, for example an apartment number. | [optional]
**postal_code** | **String** | A postal code. | 
**city** | **String** | The recipient's city. | 
**region** | Option<**String**> | The recipient's region. | [optional]
**country** | **String** | A country code in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format. | 
**locale** | [**models::SalesInvoiceRecipientLocaleResponse**](SalesInvoiceRecipientLocaleResponse.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


