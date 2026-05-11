# \MandatesApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_mandate**](MandatesApiApi.md#create_mandate) | **POST** /v2/customers/{customerId}/mandates | Create mandate
[**get_mandate**](MandatesApiApi.md#get_mandate) | **GET** /v2/customers/{customerId}/mandates/{mandateId} | Get mandate
[**list_mandates**](MandatesApiApi.md#list_mandates) | **GET** /v2/customers/{customerId}/mandates | List mandates
[**revoke_mandate**](MandatesApiApi.md#revoke_mandate) | **DELETE** /v2/customers/{customerId}/mandates/{mandateId} | Revoke mandate



## create_mandate

> models::MandateResponse create_mandate(customer_id, idempotency_key, mandate_request)
Create mandate

Create a mandate for a specific customer. Mandates allow you to charge a customer's card, PayPal account or bank account recurrently.  It is only possible to create mandates for IBANs and PayPal billing agreements with this endpoint. To create mandates for cards, your customers need to perform a 'first payment' with their card.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**mandate_request** | Option<[**MandateRequest**](MandateRequest.md)> |  |  |

### Return type

[**models::MandateResponse**](mandate-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_mandate

> models::MandateResponse get_mandate(customer_id, mandate_id, testmode, idempotency_key)
Get mandate

Retrieve a single mandate by its ID. Depending on the type of mandate, the object will contain the customer's bank account details, card details, or PayPal account details.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**mandate_id** | **String** | Provide the ID of the related mandate. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::MandateResponse**](mandate-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_mandates

> models::ListMandates200Response list_mandates(customer_id, from, limit, sort, scopes, testmode, idempotency_key)
List mandates

Retrieve a list of all mandates.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<[**Sorting**](Sorting.md)> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**scopes** | Option<[**Vec<models::MandateScopes>**](Models__MandateScopes.md)> | Returns only mandates that include the specified scopes. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListMandates200Response**](list_mandates_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## revoke_mandate

> revoke_mandate(customer_id, mandate_id, idempotency_key, delete_payment_link_request)
Revoke mandate

Revoke a customer's mandate. You will no longer be able to charge the customer's bank account or card with this mandate, and all connected subscriptions will be canceled.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**customer_id** | **String** | Provide the ID of the related customer. | [required] |
**mandate_id** | **String** | Provide the ID of the related mandate. | [required] |
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

