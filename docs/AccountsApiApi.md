# \AccountsApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_business_account**](AccountsApiApi.md#get_business_account) | **GET** /v2/business-accounts/accounts/{businessAccountId} | Get business account
[**get_business_account_transaction**](AccountsApiApi.md#get_business_account_transaction) | **GET** /v2/business-accounts/accounts/{businessAccountId}/transactions/{transactionId} | Get transaction
[**list_business_account_transactions**](AccountsApiApi.md#list_business_account_transactions) | **GET** /v2/business-accounts/accounts/{businessAccountId}/transactions | List transactions
[**list_business_accounts**](AccountsApiApi.md#list_business_accounts) | **GET** /v2/business-accounts/accounts | List business accounts



## get_business_account

> models::BusinessAccountResponse get_business_account(business_account_id, testmode, idempotency_key)
Get business account

Retrieve a single business account object by its account ID. This allows you to check the current status, balance, and account details.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**business_account_id** | **String** | Provide the ID of the related business account. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::BusinessAccountResponse**](business-account-response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_account_transaction

> models::TransactionResponse get_business_account_transaction(business_account_id, transaction_id, testmode, idempotency_key)
Get transaction

Retrieve a single transaction object by its transaction ID. This allows you to check the details, amount, counterparty, and balance impact of a specific transaction.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**business_account_id** | **String** | Provide the ID of the related business account. | [required] |
**transaction_id** | **String** | Provide the ID of the related transaction. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::TransactionResponse**](transaction-response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_account_transactions

> models::ListBusinessAccountTransactions200Response list_business_account_transactions(business_account_id, from, limit, sort, testmode, idempotency_key)
List transactions

Retrieve all transactions for a specific business account.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**business_account_id** | **String** | Provide the ID of the related business account. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<[**Sorting**](Sorting.md)> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListBusinessAccountTransactions200Response**](list_business_account_transactions_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_accounts

> models::ListBusinessAccounts200Response list_business_accounts(from, limit, sort, testmode, idempotency_key)
List business accounts

Retrieve all business accounts for the authenticated organization.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<[**Sorting**](Sorting.md)> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListBusinessAccounts200Response**](list_business_accounts_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

