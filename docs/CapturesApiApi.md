# \CapturesApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_capture**](CapturesApiApi.md#create_capture) | **POST** /v2/payments/{paymentId}/captures | Create capture
[**get_capture**](CapturesApiApi.md#get_capture) | **GET** /v2/payments/{paymentId}/captures/{captureId} | Get capture
[**list_captures**](CapturesApiApi.md#list_captures) | **GET** /v2/payments/{paymentId}/captures | List captures



## create_capture

> models::CaptureResponse create_capture(payment_id, idempotency_key, entity_capture)
Create capture

Capture an *authorized* payment.  Some payment methods allow you to first collect a customer's authorization, and capture the amount at a later point.  By default, Mollie captures payments automatically. If however you configured your payment with `captureMode: manual`, you can capture the payment using this endpoint after having collected the customer's authorization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**entity_capture** | Option<[**EntityCapture**](EntityCapture.md)> |  |  |

### Return type

[**models::CaptureResponse**](capture-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_capture

> models::CaptureResponse get_capture(payment_id, capture_id, embed, testmode, idempotency_key)
Get capture

Retrieve a single payment capture by its ID and the ID of its parent payment.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**capture_id** | **String** | Provide the ID of the related capture. | [required] |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::CaptureResponse**](capture-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_captures

> models::ListCaptures200Response list_captures(payment_id, from, limit, embed, testmode, idempotency_key)
List captures

Retrieve a list of all captures created for a specific payment.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListCaptures200Response**](list_captures_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

