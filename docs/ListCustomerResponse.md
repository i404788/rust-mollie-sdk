# ListCustomerResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a customer object. Will always contain the string `customer` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this customer. Example: `cst_vsKJpSsabw`. | [readonly]
**mode** | [**models::Mode**](Mode.md) |  | 
**name** | **String** | The full name of the customer. | 
**email** | **String** | The email address of the customer.  If the domain contains non-ASCII characters, encode it as Punycode per [RFC 3492](https://www.rfc-editor.org/rfc/rfc3492). | 
**locale** | Option<[**models::LocaleResponse**](LocaleResponse.md)> | Preconfigure the language to be used in the hosted payment pages shown to the customer. Should only be provided if absolutely necessary. If not provided, the browser language will be used which is typically highly accurate. | 
**metadata** | Option<[**models::Metadata**](Metadata.md)> |  | 
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**_links** | [**models::ListEntityCustomerLinks**](ListEntityCustomerLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


