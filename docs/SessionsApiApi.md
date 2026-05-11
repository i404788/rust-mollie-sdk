# \SessionsApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_session**](SessionsApiApi.md#create_session) | **POST** /v2/sessions | Create session
[**get_session**](SessionsApiApi.md#get_session) | **GET** /v2/sessions/{sessionId} | Get session



## create_session

> models::SessionResponse create_session(idempotency_key, session_request)
Create session

> 🚧 Beta feature > > This feature is currently in private beta, and the final specification may still change.  Create a session to start a checkout process with Mollie Components.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**session_request** | Option<[**SessionRequest**](SessionRequest.md)> |  |  |

### Return type

[**models::SessionResponse**](session-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_session

> models::SessionResponse get_session(session_id, idempotency_key)
Get session

> 🚧 Beta feature > > This feature is currently in private beta, and the final specification may still change.  Retrieve a session to view its details and status to inform your customers about the checkout process.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**session_id** | **String** | Provide the ID of the related session. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::SessionResponse**](session-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

