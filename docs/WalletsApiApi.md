# \WalletsApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**request_apple_pay_payment_session**](WalletsApiApi.md#request_apple_pay_payment_session) | **POST** /v2/wallets/applepay/sessions | Request Apple Pay payment session



## request_apple_pay_payment_session

> std::collections::HashMap<String, serde_json::Value> request_apple_pay_payment_session(idempotency_key, request_apple_pay_payment_session_request)
Request Apple Pay payment session

When integrating Apple Pay in your own checkout on the web, you need to [provide merchant validation](https://developer.apple.com/documentation/apple_pay_on_the_web/apple_pay_js_api/providing_merchant_validation). This is normally done using Apple's [Requesting an Apple Pay Session](https://developer.apple.com/documentation/apple_pay_on_the_web/apple_pay_js_api/requesting_an_apple_pay_payment_session). The merchant validation proves to Apple that a validated merchant is calling the Apple Pay Javascript APIs.  To integrate Apple Pay via Mollie, you will have to call the Mollie API instead of Apple's API. The response of this API call can then be passed as-is to the completion method, `completeMerchantValidation`.  Before requesting an Apple Pay Payment Session, you must place the domain validation file on your server at: `https://[domain]/.well-known/apple-developer-merchantid-domain-association`. Without this file, it will not be possible to use Apple Pay on your domain.  Each new transaction requires a new payment session object. Merchant session objects are not reusable, and they expire after five minutes.  Payment sessions cannot be requested directly from the browser. The request must be sent from your server. For the full documentation, see the official [Apple Pay JS API](https://developer.apple.com/documentation/apple_pay_on_the_web/apple_pay_js_api) documentation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**request_apple_pay_payment_session_request** | Option<[**RequestApplePayPaymentSessionRequest**](RequestApplePayPaymentSessionRequest.md)> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

