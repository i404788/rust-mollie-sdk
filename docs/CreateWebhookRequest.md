# CreateWebhookRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | A name that identifies the webhook. | 
**url** | **String** | The URL Mollie will send the events to. This URL must be publicly accessible. | 
**event_types** | [**models::WebhookEventTypes**](webhook-event-types.md) | The list of events to enable for this webhook. You may specify `'*'` to add all events, except those that require explicit selection. Separate multiple event types with a comma. | 
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


