# UpdateWebhookRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> | A name that identifies the webhook. | [optional]
**url** | Option<**String**> | The URL Mollie will send the events to. This URL must be publicly accessible. | [optional]
**event_types** | Option<[**models::CreateWebhookRequestEventTypes**](CreateWebhookRequestEventTypes.md)> |  | [optional]
**testmode** | Option<**bool**> | Whether the entity was created in test mode or live mode. This field does not update the mode of the entity.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


