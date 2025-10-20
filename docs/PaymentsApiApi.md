# \PaymentsApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_payment**](PaymentsApiApi.md#cancel_payment) | **DELETE** /payments/{paymentId} | Cancel payment
[**create_payment**](PaymentsApiApi.md#create_payment) | **POST** /payments | Create payment
[**get_payment**](PaymentsApiApi.md#get_payment) | **GET** /payments/{paymentId} | Get payment
[**list_payments**](PaymentsApiApi.md#list_payments) | **GET** /payments | List payments
[**release_authorization**](PaymentsApiApi.md#release_authorization) | **POST** /payments/{paymentId}/release-authorization | Release payment authorization
[**update_payment**](PaymentsApiApi.md#update_payment) | **PATCH** /payments/{paymentId} | Update payment



## cancel_payment

> models::PaymentResponse cancel_payment(payment_id, idempotency_key, cancel_payment_request)
Cancel payment

Depending on the payment method, you may be able to cancel a payment for a certain amount of time — usually until the next business day or as long as the payment status is open.  Payments may also be canceled manually from the Mollie Dashboard.  The `isCancelable` property on the [Payment object](get-payment) will indicate if the payment can be canceled.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**cancel_payment_request** | Option<[**CancelPaymentRequest**](CancelPaymentRequest.md)> |  |  |

### Return type

[**models::PaymentResponse**](payment-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_payment

> models::PaymentResponse create_payment(include, idempotency_key, payment_request)
Create payment

Payment creation is elemental to the Mollie API: this is where most payment implementations start off.  Once you have created a payment, you should redirect your customer to the URL in the `_links.checkout` property from the response.  To wrap your head around the payment process, an explanation and flow charts can be found in the 'Accepting payments' guide.  If you specify the `method` parameter when creating a payment, optional additional parameters may be available for the payment method that are not listed below. Please refer to the guide on [method-specific parameters](extra-payment-parameters).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**include** | Option<**String**> | This endpoint allows you to include additional information via the `include` query string parameter. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**payment_request** | Option<[**PaymentRequest**](PaymentRequest.md)> |  |  |

### Return type

[**models::PaymentResponse**](payment-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_payment

> models::PaymentResponse get_payment(payment_id, include, embed, testmode, idempotency_key)
Get payment

Retrieve a single payment object by its payment ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**include** | Option<**String**> | This endpoint allows you to include additional information via the `include` query string parameter. |  |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::PaymentResponse**](payment-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_payments

> models::ListSettlementPayments200Response list_payments(from, limit, sort, profile_id, testmode, idempotency_key)
List payments

Retrieve all payments created with the current website profile.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<**String**> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) you wish to retrieve the resources for.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSettlementPayments200Response**](list_settlement_payments_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## release_authorization

> serde_json::Value release_authorization(payment_id, idempotency_key, release_authorization_request)
Release payment authorization

Releases the full remaining authorized amount. Call this endpoint when you will not be making any additional captures. Payment authorizations may also be released manually from the Mollie Dashboard.  Mollie will do its best to process release requests, but it is not guaranteed that it will succeed. It is up to the issuing bank if and when the hold will be released.  If the request does succeed, the payment status will change to `canceled` for payments without captures. If there is a successful capture, the payment will transition to `paid`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**release_authorization_request** | Option<[**ReleaseAuthorizationRequest**](ReleaseAuthorizationRequest.md)> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_payment

> models::PaymentResponse update_payment(payment_id, idempotency_key, update_payment_request)
Update payment

Certain details of an existing payment can be updated.  Updating the payment details will not result in a webhook call.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**update_payment_request** | Option<[**UpdatePaymentRequest**](UpdatePaymentRequest.md)> |  |  |

### Return type

[**models::PaymentResponse**](payment-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

