# \SettlementsApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_next_settlement**](SettlementsApiApi.md#get_next_settlement) | **GET** /settlements/next | Get next settlement
[**get_open_settlement**](SettlementsApiApi.md#get_open_settlement) | **GET** /settlements/open | Get open settlement
[**get_settlement**](SettlementsApiApi.md#get_settlement) | **GET** /settlements/{id} | Get settlement
[**list_settlement_captures**](SettlementsApiApi.md#list_settlement_captures) | **GET** /settlements/{settlementId}/captures | List settlement captures
[**list_settlement_chargebacks**](SettlementsApiApi.md#list_settlement_chargebacks) | **GET** /settlements/{settlementId}/chargebacks | List settlement chargebacks
[**list_settlement_payments**](SettlementsApiApi.md#list_settlement_payments) | **GET** /settlements/{settlementId}/payments | List settlement payments
[**list_settlement_refunds**](SettlementsApiApi.md#list_settlement_refunds) | **GET** /settlements/{settlementId}/refunds | List settlement refunds
[**list_settlements**](SettlementsApiApi.md#list_settlements) | **GET** /settlements | List settlements



## get_next_settlement

> models::EntitySettlement get_next_settlement(idempotency_key)
Get next settlement

Retrieve the details of the current settlement, that has not yet been paid out.  For a complete reference of the settlement object, refer to the [Get settlement endpoint](get-settlement) documentation.  For more accurate bookkeeping, refer to the [balance report](get-balance-report) endpoint or the [balance transactions](list-balance-transactions) endpoint.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntitySettlement**](entity-settlement.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_open_settlement

> models::EntitySettlement get_open_settlement(idempotency_key)
Get open settlement

Retrieve the details of the open balance of the organization. This will return a settlement object representing your organization's balance.  For a complete reference of the settlement object, refer to the [Get settlement endpoint](get-settlement) documentation.  For more accurate bookkeeping, refer to the [balance report](get-balance-report) endpoint or the [balance transactions](list-balance-transactions) endpoint.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntitySettlement**](entity-settlement.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_settlement

> models::EntitySettlement get_settlement(id, idempotency_key)
Get settlement

Retrieve a single settlement by its ID.  To lookup settlements by their bank reference, replace the ID in the URL by a reference. For example: `1234567.2404.03`.  A settlement represents a transfer of your balance funds to your external bank account.  Settlements will typically include a report that details what balance transactions have taken place between this settlement and the previous one.  For more accurate bookkeeping, refer to the [balance report](get-balance-report) endpoint or the [balance transactions](list-balance-transactions) endpoint.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntitySettlement**](entity-settlement.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_settlement_captures

> models::ListSettlementCaptures200Response list_settlement_captures(settlement_id, from, limit, embed, testmode, idempotency_key)
List settlement captures

Retrieve all captures included in the given settlement.  The response is in the same format as the response of the [List captures endpoint](list-captures).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**settlement_id** | **String** | Provide the ID of the related settlement. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSettlementCaptures200Response**](list_settlement_captures_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_settlement_chargebacks

> models::ListSettlementChargebacks200Response list_settlement_chargebacks(settlement_id, from, limit, embed, testmode, idempotency_key)
List settlement chargebacks

Retrieve all chargebacks 'deducted' from the given settlement.  The response is in the same format as the response of the [List chargebacks endpoint](list-chargebacks).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**settlement_id** | **String** | Provide the ID of the related settlement. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSettlementChargebacks200Response**](list_settlement_chargebacks_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_settlement_payments

> models::ListSettlementPayments200Response list_settlement_payments(settlement_id, from, limit, sort, profile_id, testmode, idempotency_key)
List settlement payments

Retrieve all payments included in the given settlement.  The response is in the same format as the response of the [List payments endpoint](list-payments).  For capture-based payment methods such as Klarna, the payments are not listed here. Refer to the [List captures endpoint](list-captures) endpoint instead.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**settlement_id** | **String** | Provide the ID of the related settlement. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<**String**> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) you wish to retrieve the resources for.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSettlementPayments200Response**](list_settlement_payments_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_settlement_refunds

> models::ListSettlementRefunds200Response list_settlement_refunds(settlement_id, from, limit, embed, testmode, idempotency_key)
List settlement refunds

Retrieve all refunds 'deducted' from the given settlement.  The response is in the same format as the response of the [List refunds endpoint](list-refunds).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**settlement_id** | **String** | Provide the ID of the related settlement. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSettlementRefunds200Response**](list_settlement_refunds_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_settlements

> models::ListSettlements200Response list_settlements(from, limit, balance_id, year, month, currencies, idempotency_key)
List settlements

Retrieve a list of all your settlements.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**balance_id** | Option<**String**> | Provide the token of the balance to filter the settlements by. This is the balance token that the settlement was settled to. |  |
**year** | Option<**String**> | Provide the year to query the settlements. Must be used combined with `month` parameter |  |
**month** | Option<**String**> | Provide the month to query the settlements. Must be used combined with `year` parameter |  |
**currencies** | Option<**Currencies**> | Provides the currencies to retrieve the settlements. It accepts multiple currencies in a comma-separated format. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSettlements200Response**](list_settlements_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

