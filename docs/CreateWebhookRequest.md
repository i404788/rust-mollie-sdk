# CreateWebhookRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | A name that identifies the webhook. | 
**url** | **String** | The URL Mollie will send the events to. This URL must be publicly accessible. | 
**event_types** | [**models::CreateWebhookRequestEventTypes**](CreateWebhookRequestEventTypes.md) |  | 
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  You can enable test mode by setting `testmode` to `true`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


