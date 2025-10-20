# \CustomersApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_customer**](CustomersApiApi.md#create_customer) | **POST** /customers | Create customer
[**create_customer_payment**](CustomersApiApi.md#create_customer_payment) | **POST** /customers/{customerId}/payments | Create customer payment
[**delete_customer**](CustomersApiApi.md#delete_customer) | **DELETE** /customers/{customerId} | Delete customer
[**get_customer**](CustomersApiApi.md#get_customer) | **GET** /customers/{customerId} | Get customer
[**list_customer_payments**](CustomersApiApi.md#list_customer_payments) | **GET** /customers/{customerId}/payments | List customer payments
[**list_customers**](CustomersApiApi.md#list_customers) | **GET** /customers | List customers
[**update_customer**](CustomersApiApi.md#update_customer) | **PATCH** /customers/{customerId} | Update customer



## create_customer

> models::CustomerResponse create_customer(idempotency_key, entity_customer)
Create customer

Creates a simple minimal representation of a customer. Payments, recurring mandates, and subscriptions can be linked to this customer object, which simplifies management of recurring payments.  Once registered, customers will also appear in your Mollie dashboard.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**entity_customer** | Option<[**EntityCustomer**](EntityCustomer.md)> |  |  |

### Return type

[**models::CustomerResponse**](customer-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_customer_payment

> models::PaymentResponse create_customer_payment(customer_id, idempotency_key, payment_request)
Create customer payment

Creates a payment for the customer.  Linking customers to payments enables you to:  * Keep track of payment preferences for your customers * Allow your customers to charge a previously used credit card with a single click in our hosted checkout * Improve payment insights in the Mollie dashboard * Use recurring payments  This endpoint is effectively an alias of the [Create payment endpoint](create-payment) with the `customerId` parameter predefined.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
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


## delete_customer

> serde_json::Value delete_customer(customer_id, idempotency_key, delete_webhook_request)
Delete customer

Delete a customer. All mandates and subscriptions created for this customer will be canceled as well.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**delete_webhook_request** | Option<[**DeleteWebhookRequest**](DeleteWebhookRequest.md)> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_customer

> models::GetCustomer200Response get_customer(customer_id, include, testmode, idempotency_key)
Get customer

Retrieve a single customer by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**include** | Option<**String**> | This endpoint allows you to include additional information via the `include` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::GetCustomer200Response**](get_customer_200_response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_customer_payments

> models::ListSettlementPayments200Response list_customer_payments(customer_id, from, limit, sort, profile_id, testmode, idempotency_key)
List customer payments

Retrieve all payments linked to the customer.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
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


## list_customers

> models::ListCustomers200Response list_customers(from, limit, sort, testmode, idempotency_key)
List customers

Retrieve a list of all customers.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<**String**> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListCustomers200Response**](list_customers_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_customer

> models::CustomerResponse update_customer(customer_id, idempotency_key, entity_customer)
Update customer

Update an existing customer.  For an in-depth explanation of each parameter, refer to the [Create customer](create-customer) endpoint.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**entity_customer** | Option<[**EntityCustomer**](EntityCustomer.md)> |  |  |

### Return type

[**models::CustomerResponse**](customer-response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

