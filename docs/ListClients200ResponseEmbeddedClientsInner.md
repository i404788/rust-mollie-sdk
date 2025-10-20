# ListClients200ResponseEmbeddedClientsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a client object. Will always contain the string `client` for this resource type. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this client. Example: `org_12345678`. | [optional][readonly]
**commission** | Option<[**models::EntityClientCommission**](entity_client_commission.md)> |  | [optional]
**organization_created_at** | Option<**String**> | The date and time the client organization was created, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | Option<[**models::EntityClientLinks**](entity_client__links.md)> |  | [optional]
**_embedded** | Option<[**models::ListClients200ResponseEmbeddedClientsInnerAllOfEmbedded**](list_clients_200_response__embedded_clients_inner_allOf__embedded.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


