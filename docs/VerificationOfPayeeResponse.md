# VerificationOfPayeeResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a payee verification object. Will always contain the string `business-account-payee-verification` for this endpoint. | [readonly]
**mode** | [**models::Mode**](Mode.md) |  | 
**creditor_bank_account** | [**models::CreditorBankAccountResponse**](CreditorBankAccountResponse.md) | The bank account details of the creditor that were verified. | 
**verification_result** | [**models::VerificationOfPayeeResponseVerificationResult**](VerificationOfPayeeResponseVerificationResult.md) |  | 
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


