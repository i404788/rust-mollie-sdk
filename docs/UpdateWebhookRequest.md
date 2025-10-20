# UpdateWebhookRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> | A name that identifies the webhook. | [optional]
**url** | Option<**String**> | The URL Mollie will send the events to. This URL must be publicly accessible. | [optional]
**event_types** | Option<[**models::WebhookEventTypes**](webhook-event-types.md)> | The list of events to enable for this webhook. You may specify `'*'` to add all events, except those that require explicit selection. Separate multiple event types with a comma. | [optional]
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


