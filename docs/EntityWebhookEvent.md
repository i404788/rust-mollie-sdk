# EntityWebhookEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a webhook event object. Will always contain the string `event` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this event. | [readonly]
**r#type** | [**models::WebhookEventTypesResponse**](WebhookEventTypesResponse.md) |  | [readonly]
**entity_id** | **String** | The entity token that triggered the event | [readonly]
**created_at** | **String** | The event's date time of creation. | [readonly]
**_embedded** | Option<[**models::EntityWebhookEventEmbedded**](EntityWebhookEventEmbedded.md)> |  | [optional]
**_links** | [**models::EntityWebhookEventLinks**](EntityWebhookEventLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


