# EntityOrganization

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains an organization object. Will always contain the string `organization` for this resource type. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this organization. Example: `org_12345678`. | [optional][readonly]
**name** | Option<**String**> | The name of the organization. | [optional][readonly]
**email** | Option<**String**> | The email address associated with the organization. | [optional][readonly]
**locale** | Option<[**models::LocaleResponse**](locale-response.md)> | The preferred locale of the merchant, as set in their Mollie dashboard. | [optional][readonly]
**address** | Option<[**models::Address**](address.md)> | The address of the organization. | [optional]
**registration_number** | Option<**String**> | The registration number of the organization at their local chamber of commerce. | [optional]
**vat_number** | Option<**String**> | The VAT number of the organization, if based in the European Union or in The United Kingdom. VAT numbers are verified against the international registry *VIES*.  The field is not present for merchants residing in other countries. | [optional]
**vat_regulation** | Option<[**models::OrganizationVatRegulation**](organization-vat-regulation.md)> |  | [optional]
**_links** | Option<[**models::EntityOrganizationLinks**](entity_organization__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


