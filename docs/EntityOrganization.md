# EntityOrganization

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains an organization object. Will always contain the string `organization` for this resource type. | [readonly]
**id** | **String** |  | [readonly]
**name** | **String** | The name of the organization. | [readonly]
**email** | **String** | The email address associated with the organization.  If the domain contains non-ASCII characters, encode it as Punycode per [RFC 3492](https://www.rfc-editor.org/rfc/rfc3492). | [readonly]
**locale** | Option<[**models::LocaleResponse**](LocaleResponse.md)> | The preferred locale of the merchant, as set in their Mollie dashboard. | [readonly]
**address** | [**models::Address**](Address.md) | The address of the organization. | 
**registration_number** | **String** | The registration number of the organization at their local chamber of commerce. | 
**vat_number** | Option<**String**> | The VAT number of the organization, if based in the European Union or in The United Kingdom. VAT numbers are verified against the international registry *VIES*.  The field is not present for merchants residing in other countries. | [optional]
**vat_regulation** | Option<[**models::OrganizationVatRegulation**](OrganizationVatRegulation.md)> |  | [optional]
**_links** | [**models::EntityOrganizationLinks**](EntityOrganizationLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


