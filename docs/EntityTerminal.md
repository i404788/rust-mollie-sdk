# EntityTerminal

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a terminal object. Will always contain the string `terminal` for this endpoint. | [readonly]
**id** | **String** |  | 
**mode** | [**models::Mode**](mode.md) |  | 
**description** | **String** | A short description of the terminal. The description can be used as an identifier for the terminal. Currently, the description is set when the terminal is initially configured. It will be visible in the Mollie Dashboard, and it may be visible on the device itself depending on the device. | 
**status** | [**models::TerminalStatus**](terminal-status.md) |  | [readonly]
**brand** | Option<[**models::TerminalBrand**](terminal-brand.md)> |  | 
**model** | Option<[**models::TerminalModel**](terminal-model.md)> |  | 
**serial_number** | Option<**String**> | The serial number of the terminal. The serial number is provided at terminal creation time. | 
**currency** | **String** | The currency configured on the terminal, in ISO 4217 format. Currently most of our terminals are bound to a specific currency, chosen during setup. | 
**profile_id** | **String** | The identifier referring to the [profile](get-profile) this entity belongs to.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted in the creation request. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. | 
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**updated_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | 
**_links** | [**models::EntityWebhookLinks**](entity_webhook__links.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


