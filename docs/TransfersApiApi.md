# \TransfersApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_transfer**](TransfersApiApi.md#create_transfer) | **POST** /v2/business-accounts/transfers | Create transfer
[**get_transfer**](TransfersApiApi.md#get_transfer) | **GET** /v2/business-accounts/transfers/{businessAccountsTransferId} | Get transfer



## create_transfer

> models::TransferResponse create_transfer(x_client_signature, x_client_signed_at, idempotency_key, idempotency_key2, transfer_request)
Create transfer

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Create a SEPA Credit Transfer from your Mollie Business Account.  To initiate a transfer, you must provide the transfer scheme, the amount, the debtor IBAN (your Mollie Business Account IBAN), and the creditor (recipient) details.  Each request must include an `Idempotency-Key` header to prevent duplicate transfers, and must be signed using the `X-Client-Signature` and `X-Client-Signed-At` headers.  ### Simulating transfer scenarios in test mode  In test mode, you can simulate various transfer scenarios by adjusting the transfer amount. This allows you to mimic the typical status progression of a real-world transfer. Note that a transfer's progression will stop once it reaches a final status: `blocked`, `failed`, `processed`, or `returned`.  | Amount  | Scenario                                            | Webhook sequence                                                                                                                                                   | |---------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------| | `11.00` | Transfer initiated, pending review by Mollie        | `business-account-transfer.requested` → `business-account-transfer.initiated` → `business-account-transfer.pending-review`                                         | | `12.00` | Transfer initiated, blocked by Mollie               | `business-account-transfer.requested` → `business-account-transfer.initiated` → `business-account-transfer.pending-review` → `business-account-transfer.blocked`   | | `13.00` | Transfer initiated, failed on scheme submission     | `business-account-transfer.requested` → `business-account-transfer.initiated` → `business-account-transfer.failed`                                                 | | `14.00` | Transfer processed, then returned by receiving bank | `business-account-transfer.requested` → `business-account-transfer.initiated` → `business-account-transfer.processed` → `business-account-transfer.returned`       | | Other   | Default: transfer is processed                      | `business-account-transfer.requested` → `business-account-transfer.initiated` → `business-account-transfer.processed`                                              |

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**x_client_signature** | **String** | A cryptographic signature of the request payload, used to verify the authenticity of the transfer request. | [required] |
**x_client_signed_at** | **String** | The timestamp (in ISO 8601 format) indicating when the client signed the request. Used in conjunction with `X-Client-Signature` for request verification. | [required] |
**idempotency_key** | **String** | A unique value used to identify this request and prevent duplicate transfers. UUIDv4 is recommended to guarantee uniqueness across multiple processes or servers. If two requests are received with the same idempotency key, the second request will be discarded.  View the [public documentation](https://docs.mollie.com/reference/api-idempotency#using-an-idempotency-key) to learn more. | [required] |
**idempotency_key2** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**transfer_request** | Option<[**TransferRequest**](TransferRequest.md)> |  |  |

### Return type

[**models::TransferResponse**](transfer-response.md)

### Authorization

[organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_transfer

> models::TransferResponse get_transfer(business_accounts_transfer_id, testmode, idempotency_key)
Get transfer

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Retrieve a single transfer object by its transfer ID. This allows you to check the current status and details of a previously created transfer.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**business_accounts_transfer_id** | **String** | Provide the ID of the related transfer. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::TransferResponse**](transfer-response.md)

### Authorization

[organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

