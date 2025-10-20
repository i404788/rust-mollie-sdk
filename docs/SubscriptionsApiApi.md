# \SubscriptionsApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_subscription**](SubscriptionsApiApi.md#cancel_subscription) | **DELETE** /customers/{customerId}/subscriptions/{subscriptionId} | Cancel subscription
[**create_subscription**](SubscriptionsApiApi.md#create_subscription) | **POST** /customers/{customerId}/subscriptions | Create subscription
[**get_subscription**](SubscriptionsApiApi.md#get_subscription) | **GET** /customers/{customerId}/subscriptions/{subscriptionId} | Get subscription
[**list_all_subscriptions**](SubscriptionsApiApi.md#list_all_subscriptions) | **GET** /subscriptions | List all subscriptions
[**list_subscription_payments**](SubscriptionsApiApi.md#list_subscription_payments) | **GET** /customers/{customerId}/subscriptions/{subscriptionId}/payments | List subscription payments
[**list_subscriptions**](SubscriptionsApiApi.md#list_subscriptions) | **GET** /customers/{customerId}/subscriptions | List customer subscriptions
[**update_subscription**](SubscriptionsApiApi.md#update_subscription) | **PATCH** /customers/{customerId}/subscriptions/{subscriptionId} | Update subscription



## cancel_subscription

> models::SubscriptionResponse cancel_subscription(customer_id, subscription_id, idempotency_key, delete_webhook_request)
Cancel subscription

Cancel an existing subscription. Canceling a subscription has no effect on the mandates of the customer.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**subscription_id** | **String** | Provide the ID of the related subscription. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**delete_webhook_request** | Option<[**DeleteWebhookRequest**](DeleteWebhookRequest.md)> |  |  |

### Return type

[**models::SubscriptionResponse**](subscription-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_subscription

> models::SubscriptionResponse create_subscription(customer_id, idempotency_key, subscription_request)
Create subscription

With subscriptions, you can schedule recurring payments to take place at regular intervals.  For example, by simply specifying an `amount` and an `interval`, you can create an endless subscription to charge a monthly fee, until you cancel the subscription.  Or, you could use the times parameter to only charge a limited number of times, for example to split a big transaction in multiple parts.  A few example usages:  `amount[currency]=\"EUR\"` `amount[value]=\"5.00\"` `interval=\"2 weeks\"` Your customer will be charged €5 once every two weeks.  `amount[currency]=\"EUR\"` `amount[value]=\"20.00\"` `interval=\"1 day\" times=5` Your customer will be charged €20 every day, for five consecutive days.  `amount[currency]=\"EUR\"` `amount[value]=\"10.00\"` `interval=\"1 month\"` `startDate=\"2018-04-30\"` Your customer will be charged €10 on the last day of each month, starting in April 2018.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**subscription_request** | Option<[**SubscriptionRequest**](SubscriptionRequest.md)> |  |  |

### Return type

[**models::SubscriptionResponse**](subscription-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_subscription

> models::SubscriptionResponse get_subscription(customer_id, subscription_id, testmode, idempotency_key)
Get subscription

Retrieve a single subscription by its ID and the ID of its parent customer.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**subscription_id** | **String** | Provide the ID of the related subscription. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::SubscriptionResponse**](subscription-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_all_subscriptions

> models::ListAllSubscriptions200Response list_all_subscriptions(from, limit, profile_id, testmode, idempotency_key)
List all subscriptions

Retrieve all subscriptions initiated across all your customers.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) you wish to retrieve subscriptions for.  Most API credentials are linked to a single profile. In these cases the `profileId` is already implied.  To retrieve all subscriptions across the organization, use an organization-level API credential and omit the `profileId` parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListAllSubscriptions200Response**](list_all_subscriptions_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_subscription_payments

> models::ListSettlementPayments200Response list_subscription_payments(customer_id, subscription_id, from, limit, sort, profile_id, testmode, idempotency_key)
List subscription payments

Retrieve all payments of a specific subscription.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**subscription_id** | **String** | Provide the ID of the related subscription. | [required] |
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


## list_subscriptions

> models::ListSubscriptions200Response list_subscriptions(customer_id, from, limit, sort, testmode, idempotency_key)
List customer subscriptions

Retrieve all subscriptions of a customer.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<**String**> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSubscriptions200Response**](list_subscriptions_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_subscription

> models::SubscriptionResponse update_subscription(customer_id, subscription_id, idempotency_key, update_subscription_request)
Update subscription

Update an existing subscription.  Canceled subscriptions cannot be updated.  For an in-depth explanation of each parameter, refer to the [Create subscription](create-subscription) endpoint.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**subscription_id** | **String** | Provide the ID of the related subscription. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**update_subscription_request** | Option<[**UpdateSubscriptionRequest**](UpdateSubscriptionRequest.md)> |  |  |

### Return type

[**models::SubscriptionResponse**](subscription-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

