# \PaymentLinksApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_payment_link**](PaymentLinksApiApi.md#create_payment_link) | **POST** /v2/payment-links | Create payment link
[**delete_payment_link**](PaymentLinksApiApi.md#delete_payment_link) | **DELETE** /v2/payment-links/{paymentLinkId} | Delete payment link
[**get_payment_link**](PaymentLinksApiApi.md#get_payment_link) | **GET** /v2/payment-links/{paymentLinkId} | Get payment link
[**get_payment_link_payments**](PaymentLinksApiApi.md#get_payment_link_payments) | **GET** /v2/payment-links/{paymentLinkId}/payments | Get payment link payments
[**list_payment_links**](PaymentLinksApiApi.md#list_payment_links) | **GET** /v2/payment-links | List payment links
[**update_payment_link**](PaymentLinksApiApi.md#update_payment_link) | **PATCH** /v2/payment-links/{paymentLinkId} | Update payment link



## create_payment_link

> models::PaymentLinkResponse create_payment_link(idempotency_key, create_payment_link_request)
Create payment link

With the Payment links API you can generate payment links that by default, unlike regular payments, do not expire. The payment link can be shared with your customers and will redirect them to them the payment page where they can complete the payment. A [payment](get-payment) will only be created once the customer initiates the payment.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**create_payment_link_request** | Option<[**CreatePaymentLinkRequest**](CreatePaymentLinkRequest.md)> |  |  |

### Return type

[**models::PaymentLinkResponse**](payment-link-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_payment_link

> delete_payment_link(payment_link_id, idempotency_key, delete_payment_link_request)
Delete payment link

Payment links which have not been opened and no payments have been made yet can be deleted entirely. This can be useful for removing payment links that have been incorrectly configured or that are no longer relevant.  Once deleted, the payment link will no longer show up in the API or Mollie dashboard.  To simply disable a payment link without fully deleting it, you can use the `archived` parameter on the [Update payment link](update-payment-link) endpoint instead.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_link_id** | **String** | Provide the ID of the related payment link. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**delete_payment_link_request** | Option<[**DeletePaymentLinkRequest**](DeletePaymentLinkRequest.md)> |  |  |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_payment_link

> models::PaymentLinkResponse get_payment_link(payment_link_id, testmode, idempotency_key)
Get payment link

Retrieve a single payment link by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_link_id** | **String** | Provide the ID of the related payment link. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::PaymentLinkResponse**](payment-link-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_payment_link_payments

> models::ListPayments200Response get_payment_link_payments(payment_link_id, from, limit, sort, testmode, idempotency_key)
Get payment link payments

Retrieve the list of payments for a specific payment link.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_link_id** | **String** | Provide the ID of the related payment link. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<[**Sorting**](Sorting.md)> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListPayments200Response**](list_payments_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_payment_links

> models::ListPaymentLinks200Response list_payment_links(from, limit, testmode, idempotency_key)
List payment links

Retrieve a list of all payment links.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListPaymentLinks200Response**](list_payment_links_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_payment_link

> models::PaymentLinkResponse update_payment_link(payment_link_id, idempotency_key, update_payment_link_request)
Update payment link

Certain details of an existing payment link can be updated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_link_id** | **String** | Provide the ID of the related payment link. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**update_payment_link_request** | Option<[**UpdatePaymentLinkRequest**](UpdatePaymentLinkRequest.md)> |  |  |

### Return type

[**models::PaymentLinkResponse**](payment-link-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

