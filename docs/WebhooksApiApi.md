# \WebhooksApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_webhook**](WebhooksApiApi.md#create_webhook) | **POST** /webhooks | Create a webhook
[**delete_webhook**](WebhooksApiApi.md#delete_webhook) | **DELETE** /webhooks/{id} | Delete a webhook
[**get_webhook**](WebhooksApiApi.md#get_webhook) | **GET** /webhooks/{id} | Get a webhook
[**list_webhooks**](WebhooksApiApi.md#list_webhooks) | **GET** /webhooks | List all webhooks
[**test_webhook**](WebhooksApiApi.md#test_webhook) | **POST** /webhooks/{id}/ping | Test a webhook
[**update_webhook**](WebhooksApiApi.md#update_webhook) | **PATCH** /webhooks/{id} | Update a webhook



## create_webhook

> models::CreateWebhook create_webhook(idempotency_key, create_webhook_request)
Create a webhook

A webhook must have a name, an url and a list of event types. You can also create webhooks in the webhooks settings section of the Dashboard.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**create_webhook_request** | Option<[**CreateWebhookRequest**](CreateWebhookRequest.md)> |  |  |

### Return type

[**models::CreateWebhook**](create-webhook.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_webhook

> serde_json::Value delete_webhook(id, idempotency_key, delete_webhook_request)
Delete a webhook

Delete a single webhook object by its webhook ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**delete_webhook_request** | Option<[**DeleteWebhookRequest**](DeleteWebhookRequest.md)> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_webhook

> models::EntityWebhook get_webhook(id, testmode, idempotency_key)
Get a webhook

Retrieve a single webhook object by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityWebhook**](entity-webhook.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_webhooks

> models::ListWebhooks200Response list_webhooks(from, limit, sort, event_types, testmode, idempotency_key)
List all webhooks

Returns a paginated list of your webhooks. If no webhook endpoints are available, the resulting array will be empty. This request should never throw an error.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<**String**> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**event_types** | Option<[**WebhookEventTypes**](.md)> | Used to filter out only the webhooks that are subscribed to certain types of events. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListWebhooks200Response**](list_webhooks_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## test_webhook

> serde_json::Value test_webhook(id, idempotency_key, delete_webhook_request)
Test a webhook

Sends a test event to the webhook to verify the endpoint is working as expected.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**delete_webhook_request** | Option<[**DeleteWebhookRequest**](DeleteWebhookRequest.md)> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_webhook

> models::EntityWebhook update_webhook(id, idempotency_key, update_webhook_request)
Update a webhook

Updates the webhook. You may edit the name, url and the list of subscribed event types.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**update_webhook_request** | Option<[**UpdateWebhookRequest**](UpdateWebhookRequest.md)> |  |  |

### Return type

[**models::EntityWebhook**](entity-webhook.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

