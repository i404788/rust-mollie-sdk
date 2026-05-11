# \VerifyPayeeApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**verify_payee**](VerifyPayeeApiApi.md#verify_payee) | **POST** /v2/business-accounts/payee-verifications | Verify Payee



## verify_payee

> models::VerificationOfPayeeResponse verify_payee(idempotency_key, verification_of_payee_request)
Verify Payee

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Perform a Verification of Payee (VoP) check. This allows you to verify the account holder name against the records held by the receiving bank before initiating a transfer.  The verification result indicates whether the provided name matches, closely matches, or does not match the name on file at the receiving bank. This helps prevent misdirected payments.  ### Simulating verification scenarios in test mode  In test mode, you can simulate various verification outcomes by adjusting the creditor name in the `creditorBankAccount.accountHolderName` property. This allows you to test all possible Verification of Payee results without needing special properties. The names are case insensitive.  | Account holder name                    | Scenario                                      | Verification result | Suggested name | |----------------------------------------|-----------------------------------------------|---------------------|----------------| | `John Close Match`                     | Name closely matches the bank records          | `close-match`       | `John Match`   | | `John No Match`                        | Name does not match the bank records           | `no-match`          | —              | | `John Unavailable`                     | Verification is not available                  | `not-available`     | —              | | Any other name                         | Default: name matches the bank records         | `match`             | —              |

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**verification_of_payee_request** | Option<[**VerificationOfPayeeRequest**](VerificationOfPayeeRequest.md)> |  |  |

### Return type

[**models::VerificationOfPayeeResponse**](verification-of-payee-response.md)

### Authorization

[organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

