# \BalancesApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_balance**](BalancesApiApi.md#get_balance) | **GET** /v2/balances/{balanceId} | Get balance
[**get_balance_report**](BalancesApiApi.md#get_balance_report) | **GET** /v2/balances/{balanceId}/report | Get balance report
[**get_primary_balance**](BalancesApiApi.md#get_primary_balance) | **GET** /v2/balances/primary | Get primary balance
[**list_balance_transactions**](BalancesApiApi.md#list_balance_transactions) | **GET** /v2/balances/{balanceId}/transactions | List balance transactions
[**list_balances**](BalancesApiApi.md#list_balances) | **GET** /v2/balances | List balances



## get_balance

> models::EntityBalance get_balance(balance_id, testmode, idempotency_key)
Get balance

When processing payments with Mollie, we put all pending funds — usually minus Mollie fees — on a balance. Once you have linked a bank account to your Mollie account, we can pay out your balance towards this bank account.  With the Balances API you can retrieve your current balance. The response includes two amounts:  * The *pending amount*. These are payments that have been marked as `paid`, but are not yet available on your balance. * The *available amount*. This is the amount that you can get paid out to your bank account, or use for refunds.  With instant payment methods like iDEAL, payments are moved to the available balance instantly. With slower payment methods, like credit card for example, it can take a few days before the funds are available on your balance. These funds will be shown under the *pending amount* in the meanwhile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**balance_id** | **String** | Provide the ID of the related balance. | [required] |
**testmode** | Option<**bool**> | You can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityBalance**](entity-balance.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_balance_report

> models::EntityBalanceReport get_balance_report(from, until, balance_id, grouping, testmode, idempotency_key)
Get balance report

Retrieve a summarized report for all transactions on a given balance within a given timeframe.  The API also provides a detailed report on all 'prepayments' for Mollie fees that were deducted from your balance during the reported period, ahead of your Mollie invoice.  The alias `primary` can be used instead of the balance ID to refer to the organization's primary balance.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | **String** | The start date of the report, in `YYYY-MM-DD` format. The from date is 'inclusive', and in Central European Time. This means a report with for example `from=2024-01-01` will include transactions from 2024-01-01 0:00:00 CET and onwards. | [required] |
**until** | **String** | The end date of the report, in `YYYY-MM-DD` format. The until date is 'exclusive', and in Central European Time. This means a report with for example `until=2024-02-01` will include transactions up until 2024-01-31 23:59:59 CET. | [required] |
**balance_id** | **String** | Provide the ID of the related balance. | [required] |
**grouping** | Option<[**BalanceReportGrouping**](BalanceReportGrouping.md)> | You can retrieve reports in two different formats. With the `status-balances` format, transactions are grouped by status (e.g. `pending`, `available`), then by transaction type, and then by other sub-groupings where available (e.g. payment method).  With the `transaction-categories` format, transactions are grouped by transaction type, then by status, and then again by other sub-groupings where available. |  |
**testmode** | Option<**bool**> | You can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityBalanceReport**](entity-balance-report.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_primary_balance

> models::EntityBalance get_primary_balance(idempotency_key)
Get primary balance

Retrieve the primary balance. This is the balance of your account's primary currency, where all payments are settled to by default.  This endpoint is a convenient alias of the [Get balance](get-balance) endpoint.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityBalance**](entity-balance.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_balance_transactions

> models::ListBalanceTransactions200Response list_balance_transactions(balance_id, from, limit, testmode, idempotency_key)
List balance transactions

Retrieve a list of all balance transactions. Transactions include for example payments, refunds, chargebacks, and settlements.  For an aggregated report of these balance transactions, refer to the [Get balance report](get-balance-report) endpoint.  The alias `primary` can be used instead of the balance ID to refer to the organization's primary balance.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**balance_id** | **String** | Provide the ID of the related balance. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**testmode** | Option<**bool**> | You can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListBalanceTransactions200Response**](list_balance_transactions_200_response.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_balances

> models::ListBalances200Response list_balances(currency, from, limit, testmode, idempotency_key)
List balances

Retrieve a list of the organization's balances, including the primary balance.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**currency** | Option<**String**> | Optionally only return balances with the given currency. For example: `EUR`. |  |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**testmode** | Option<**bool**> | You can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListBalances200Response**](list_balances_200_response.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

