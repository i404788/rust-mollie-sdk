# ListClients200ResponseEmbeddedClientsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a client object. Will always contain the string `client` for this resource type. | [readonly]
**id** | **String** | The identifier uniquely referring to this client. Example: `org_12345678`. | [readonly]
**commission** | Option<[**models::EntityClientCommission**](EntityClientCommission.md)> |  | [optional]
**organization_created_at** | Option<**String**> | The date and time the client organization was created, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | [**models::ListEntityClientLinks**](ListEntityClientLinks.md) |  | 
**_embedded** | Option<[**models::ListClients200ResponseEmbeddedClientsInnerAllOfEmbedded**](ListClients200ResponseEmbeddedClientsInnerAllOfEmbedded.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


