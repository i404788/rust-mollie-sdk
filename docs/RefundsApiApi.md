# \RefundsApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_refund**](RefundsApiApi.md#cancel_refund) | **DELETE** /payments/{paymentId}/refunds/{refundId} | Cancel payment refund
[**create_refund**](RefundsApiApi.md#create_refund) | **POST** /payments/{paymentId}/refunds | Create payment refund
[**get_refund**](RefundsApiApi.md#get_refund) | **GET** /payments/{paymentId}/refunds/{refundId} | Get payment refund
[**list_all_refunds**](RefundsApiApi.md#list_all_refunds) | **GET** /refunds | List all refunds
[**list_refunds**](RefundsApiApi.md#list_refunds) | **GET** /payments/{paymentId}/refunds | List payment refunds



## cancel_refund

> serde_json::Value cancel_refund(payment_id, refund_id, testmode, idempotency_key)
Cancel payment refund

Refunds will be executed with a delay of two hours. Until that time, refunds may be canceled manually via the Mollie Dashboard, or by using this endpoint.  A refund can only be canceled while its `status` field is either `queued` or `pending`. See the [Get refund endpoint](get-refund) for more information.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**refund_id** | **String** | Provide the ID of the related refund. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_refund

> models::EntityRefundResponse create_refund(payment_id, idempotency_key, refund_request)
Create payment refund

Creates a refund for a specific payment. The refunded amount is credited to your customer usually either via a bank transfer or by refunding the amount to your customer's credit card.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**refund_request** | Option<[**RefundRequest**](RefundRequest.md)> |  |  |

### Return type

[**models::EntityRefundResponse**](entity-refund-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_refund

> models::EntityRefundResponse get_refund(payment_id, refund_id, embed, testmode, idempotency_key)
Get payment refund

Retrieve a single payment refund by its ID and the ID of its parent payment.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**refund_id** | **String** | Provide the ID of the related refund. | [required] |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityRefundResponse**](entity-refund-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_all_refunds

> models::ListSettlementRefunds200Response list_all_refunds(from, limit, sort, embed, profile_id, testmode, idempotency_key)
List all refunds

Retrieve a list of all of your refunds.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<**String**> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) you wish to retrieve the resources for.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSettlementRefunds200Response**](list_settlement_refunds_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_refunds

> models::ListSettlementRefunds200Response list_refunds(payment_id, from, limit, embed, testmode, idempotency_key)
List payment refunds

Retrieve a list of all refunds created for a specific payment.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSettlementRefunds200Response**](list_settlement_refunds_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

