# EntityWebhook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a webhook subscription object. Will always contain the string `webhook` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this subscription. | [readonly]
**url** | **String** | The subscription's events destination. | 
**profile_id** | Option<**String**> | The identifier uniquely referring to the profile that created the subscription. | [readonly]
**created_at** | **String** | The subscription's date time of creation. | [readonly]
**name** | **String** | The subscription's name. | 
**event_types** | [**Vec<models::WebhookEventTypesResponse>**](webhook-event-types-response.md) | The events types that are subscribed. | 
**status** | [**models::WebhookStatus**](webhook-status.md) |  | 
**mode** | [**models::Mode**](mode.md) |  | 
**_links** | [**models::EntityWebhookLinks**](entity_webhook__links.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


