# ClientLinkResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a client link object. Will always contain the string `client-link` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this client link. Example: `cl_vZCnNQsV2UtfXxYifWKWH`. | [readonly]
**owner** | Option<[**models::EntityClientLinkOwner**](EntityClientLinkOwner.md)> |  | [optional]
**name** | Option<**String**> | Name of the organization. | [optional]
**address** | Option<[**models::EntityClientLinkAddress**](EntityClientLinkAddress.md)> |  | [optional]
**registration_number** | Option<**String**> | The registration number of the organization at their local chamber of commerce. | [optional]
**vat_number** | Option<**String**> | The VAT number of the organization, if based in the European Union. VAT numbers are verified against the international registry *VIES*. | [optional]
**legal_entity** | Option<**String**> | The legal entity type of the organization, based on its country of origin. Please refer to the [legal entity list](common-data-types#legal-entity) for all possible options. | [optional]
**registration_office** | Option<**String**> | The registration office that the organization was registered at. Please refer to the [registration office list](common-data-types#registration-office) for all possible options. | [optional]
**incorporation_date** | Option<**String**> | The incorporation date of the organization (format `YYYY-MM-DD`) | [optional]
**_links** | [**models::EntityClientLinkLinks**](EntityClientLinkLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


