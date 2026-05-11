# EntityTerminal

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a terminal object. Will always contain the string `terminal` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this terminal. Example: `term_7MgL4wea46qkRcoTZjWEH`. | [readonly]
**mode** | [**models::Mode**](Mode.md) |  | 
**description** | **String** | A short description of the terminal. The description can be used as an identifier for the terminal. Currently, the description is set when the terminal is initially configured. It will be visible in the Mollie Dashboard, and it may be visible on the device itself depending on the device. | 
**status** | [**models::TerminalStatus**](TerminalStatus.md) |  | [readonly]
**brand** | Option<[**models::TerminalBrand**](TerminalBrand.md)> |  | 
**model** | Option<[**models::TerminalModel**](TerminalModel.md)> |  | 
**serial_number** | Option<**String**> | The serial number of the terminal. The serial number is provided at terminal creation time. | 
**currency** | **String** | The currency configured on the terminal, in ISO 4217 format. Currently most of our terminals are bound to a specific currency, chosen during setup. | 
**profile_id** | **String** | The identifier referring to the [profile](get-profile) this entity belongs to.  Most API credentials are linked to a single profile. In these cases the `profileId` must not be sent in the creation request. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. | 
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**updated_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | 
**_links** | [**models::EntityWebhookLinks**](EntityWebhookLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


