# \WebhookEventsApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_webhook_event**](WebhookEventsApiApi.md#get_webhook_event) | **GET** /v2/events/{webhookEventId} | Get a Webhook Event



## get_webhook_event

> models::EntityWebhookEvent get_webhook_event(webhook_event_id, testmode, idempotency_key)
Get a Webhook Event

Retrieve a single webhook event object by its event ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_event_id** | **String** | Provide the ID of the related webhook event. | [required] |
**testmode** | Option<**bool**> | You can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityWebhookEvent**](entity-webhook-event.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

