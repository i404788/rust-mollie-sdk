# \BalanceTransfersApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_connect_balance_transfer**](BalanceTransfersApiApi.md#create_connect_balance_transfer) | **POST** /v2/connect/balance-transfers | Create a Connect balance transfer
[**get_connect_balance_transfer**](BalanceTransfersApiApi.md#get_connect_balance_transfer) | **GET** /v2/connect/balance-transfers/{balanceTransferId} | Get a Connect balance transfer
[**list_connect_balance_transfers**](BalanceTransfersApiApi.md#list_connect_balance_transfers) | **GET** /v2/connect/balance-transfers | List all Connect balance transfers



## create_connect_balance_transfer

> models::EntityBalanceTransferResponse create_connect_balance_transfer(idempotency_key, entity_balance_transfer)
Create a Connect balance transfer

This API endpoint allows you to create a balance transfer from your organization's balance to a connected organization's balance, or vice versa. You can also create a balance transfer between two connected organizations. To create a balance transfer, you must be authenticated as the source organization, and the destination organization must be a connected organization that has authorized the `balance-transfers.write` scope for your organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**entity_balance_transfer** | Option<[**EntityBalanceTransfer**](EntityBalanceTransfer.md)> |  |  |

### Return type

[**models::EntityBalanceTransferResponse**](entity-balance-transfer-response.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_connect_balance_transfer

> models::EntityBalanceTransferResponse get_connect_balance_transfer(balance_transfer_id, testmode, idempotency_key)
Get a Connect balance transfer

Retrieve a single Connect balance transfer object by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**balance_transfer_id** | **String** | Provide the ID of the related balance transfer. | [required] |
**testmode** | Option<**bool**> | You can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityBalanceTransferResponse**](entity-balance-transfer-response.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_connect_balance_transfers

> models::ListConnectBalanceTransfers200Response list_connect_balance_transfers(from, limit, sort, testmode, idempotency_key)
List all Connect balance transfers

Returns a paginated list of balance transfers associated with your organization. These may be a balance transfer that was received or sent from your balance, or a balance transfer that you initiated on behalf of your clients. If no balance transfers are available, the resulting array will be empty. This request should never throw an error.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<[**Sorting**](Sorting.md)> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**testmode** | Option<**bool**> | You can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListConnectBalanceTransfers200Response**](list_connect_balance_transfers_200_response.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

