# \DelayedRoutingApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**payment_create_route**](DelayedRoutingApiApi.md#payment_create_route) | **POST** /payments/{paymentId}/routes | Create a delayed route
[**payment_list_routes**](DelayedRoutingApiApi.md#payment_list_routes) | **GET** /payments/{paymentId}/routes | List payment routes



## payment_create_route

> models::RouteCreateResponse payment_create_route(payment_id, idempotency_key, route_create_request)
Create a delayed route

Create a route for a specific payment. The routed amount is credited to the account of your customer.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**route_create_request** | Option<[**RouteCreateRequest**](RouteCreateRequest.md)> |  |  |

### Return type

[**models::RouteCreateResponse**](route-create-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## payment_list_routes

> models::PaymentListRoutes200Response payment_list_routes(payment_id, testmode, idempotency_key)
List payment routes

Retrieve a list of all routes created for a specific payment.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::PaymentListRoutes200Response**](payment_list_routes_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

