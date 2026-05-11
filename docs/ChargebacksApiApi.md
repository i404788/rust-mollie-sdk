# \ChargebacksApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_chargeback**](ChargebacksApiApi.md#get_chargeback) | **GET** /v2/payments/{paymentId}/chargebacks/{chargebackId} | Get payment chargeback
[**list_all_chargebacks**](ChargebacksApiApi.md#list_all_chargebacks) | **GET** /v2/chargebacks | List all chargebacks
[**list_chargebacks**](ChargebacksApiApi.md#list_chargebacks) | **GET** /v2/payments/{paymentId}/chargebacks | List payment chargebacks



## get_chargeback

> models::EntityChargeback get_chargeback(payment_id, chargeback_id, embed, testmode, idempotency_key)
Get payment chargeback

Retrieve a single payment chargeback by its ID and the ID of its parent payment.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**chargeback_id** | **String** | Provide the ID of the related chargeback. | [required] |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityChargeback**](entity-chargeback.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_all_chargebacks

> models::ListChargebacks200Response list_all_chargebacks(from, limit, embed, sort, profile_id, testmode, idempotency_key)
List all chargebacks

Retrieve all chargebacks initiated for all your payments.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**sort** | Option<[**Sorting**](Sorting.md)> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) you wish to retrieve chargebacks for.  Most API credentials are linked to a single profile. In these cases the `profileId` is already implied.  To retrieve all chargebacks across the organization, use an organization-level API credential and omit the `profileId` parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListChargebacks200Response**](list_chargebacks_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_chargebacks

> models::ListChargebacks200Response list_chargebacks(payment_id, from, limit, embed, testmode, idempotency_key)
List payment chargebacks

Retrieve the chargebacks initiated for a specific payment.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payment_id** | **String** | Provide the ID of the related payment. | [required] |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListChargebacks200Response**](list_chargebacks_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

