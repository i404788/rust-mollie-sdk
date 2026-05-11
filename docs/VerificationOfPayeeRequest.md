# VerificationOfPayeeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**creditor_bank_account** | [**models::CreditorBankAccount**](CreditorBankAccount.md) | The bank account details of the creditor (recipient) to verify. | 
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


