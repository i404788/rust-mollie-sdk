# \UnmatchedCreditTransfersApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_unmatched_credit_transfer**](UnmatchedCreditTransfersApiApi.md#get_unmatched_credit_transfer) | **GET** /v2/unmatched-credit-transfers/{unmatchedCreditTransferId} | Get unmatched credit transfer
[**list_unmatched_credit_transfers**](UnmatchedCreditTransfersApiApi.md#list_unmatched_credit_transfers) | **GET** /v2/unmatched-credit-transfers | List unmatched credit transfers
[**match_unmatched_credit_transfer**](UnmatchedCreditTransfersApiApi.md#match_unmatched_credit_transfer) | **POST** /v2/unmatched-credit-transfers/{unmatchedCreditTransferId}/match | Match unmatched credit transfer
[**return_unmatched_credit_transfer**](UnmatchedCreditTransfersApiApi.md#return_unmatched_credit_transfer) | **POST** /v2/unmatched-credit-transfers/{unmatchedCreditTransferId}/return | Return unmatched credit transfer



## get_unmatched_credit_transfer

> models::EntityUnmatchedCreditTransfer get_unmatched_credit_transfer(unmatched_credit_transfer_id, idempotency_key)
Get unmatched credit transfer

> 🚧 Beta feature > > This feature is currently in private beta, and the final specification may still change.  Retrieves a single unmatched credit transfer by its identifier.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**unmatched_credit_transfer_id** | **String** | Provide the ID of the related unmatched credit transfer. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityUnmatchedCreditTransfer**](entity-unmatched-credit-transfer.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_unmatched_credit_transfers

> models::ListUnmatchedCreditTransfers200Response list_unmatched_credit_transfers(from, limit, idempotency_key)
List unmatched credit transfers

> 🚧 Beta feature > > This feature is currently in private beta, and the final specification may still change.  Retrieves a list of unmatched credit transfers for the profile.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListUnmatchedCreditTransfers200Response**](list_unmatched_credit_transfers_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## match_unmatched_credit_transfer

> models::UnmatchedCreditTransferActionResponse match_unmatched_credit_transfer(unmatched_credit_transfer_id, idempotency_key, unmatched_credit_transfer_match_request)
Match unmatched credit transfer

> 🚧 Beta feature > > This feature is currently in private beta, and the final specification may still change.  Matches an unmatched credit transfer to one or more payments, settling the funds accordingly.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**unmatched_credit_transfer_id** | **String** | Provide the ID of the related unmatched credit transfer. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**unmatched_credit_transfer_match_request** | Option<[**UnmatchedCreditTransferMatchRequest**](UnmatchedCreditTransferMatchRequest.md)> |  |  |

### Return type

[**models::UnmatchedCreditTransferActionResponse**](unmatched-credit-transfer-action-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## return_unmatched_credit_transfer

> models::UnmatchedCreditTransferActionResponse return_unmatched_credit_transfer(unmatched_credit_transfer_id, idempotency_key)
Return unmatched credit transfer

> 🚧 Beta feature > > This feature is currently in private beta, and the final specification may still change.  Returns an unmatched credit transfer, sending the funds back to the original sender.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**unmatched_credit_transfer_id** | **String** | Provide the ID of the related unmatched credit transfer. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::UnmatchedCreditTransferActionResponse**](unmatched-credit-transfer-action-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

