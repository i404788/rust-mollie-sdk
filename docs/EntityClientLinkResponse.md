# EntityClientLinkResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a client link object. Will always contain the string `client-link` for this endpoint. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this client link. Example: `cl_vZCnNQsV2UtfXxYifWKWH`. | [optional][readonly]
**owner** | Option<[**models::EntityClientLinkOwner**](entity_client_link_owner.md)> |  | [optional]
**name** | Option<**String**> | Name of the organization. | [optional]
**address** | Option<[**models::EntityClientLinkAddress**](entity_client_link_address.md)> |  | [optional]
**registration_number** | Option<**String**> | The registration number of the organization at their local chamber of commerce. | [optional]
**vat_number** | Option<**String**> | The VAT number of the organization, if based in the European Union. VAT numbers are verified against the international registry *VIES*. | [optional]
**_links** | Option<[**models::EntityClientLinkLinks**](entity_client_link__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


