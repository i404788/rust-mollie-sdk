# EntityTransfer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a transfer object. Will always contain the string `business-account-transfer` for this endpoint. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this transfer. Mollie assigns this identifier at transfer creation time. | [optional][readonly]
**mode** | Option<[**models::Mode**](Mode.md)> |  | [optional]
**debtor_iban** | Option<**String**> | The IBAN of the debtor's (sender) Mollie account from which to initiate the transfer. | [optional]
**debtor** | Option<[**models::TransferParty**](TransferParty.md)> | The debtor (sender) of the transfer, including their name and account details. | [optional][readonly]
**creditor** | Option<[**models::TransferParty**](TransferParty.md)> | The creditor (recipient) of the transfer, including their name and account details. | [optional]
**amount** | Option<[**models::Amount**](Amount.md)> | The amount of the transfer, e.g. `{\"currency\":\"EUR\", \"value\":\"100.00\"}` if you would want to transfer €100.00.  Only `EUR` is supported for SEPA transfers. | [optional]
**description** | Option<**String**> | A short description of the transfer. This will appear on the bank statement of both the debtor and creditor.  It must begin with an alphanumeric character, followed by any combination of letters, numbers, spaces or special characters `/ - ? : ( ) . , ' + _`.  Constraints: - Cannot be solely a hyphen (-) or colon (:) - Cannot contain consecutive hyphens (--) - Cannot contain consecutive colons (::) | [optional]
**business_account_transaction_id** | Option<**String**> | The identifier of the corresponding transaction in the business accounts transaction resource. | [optional][readonly]
**transfer_scheme** | Option<[**models::TransferScheme**](TransferScheme.md)> |  | [optional]
**credit_debit_indicator** | Option<[**models::CreditDebitIndicator**](CreditDebitIndicator.md)> |  | [optional]
**status** | Option<[**models::TransferStatus**](TransferStatus.md)> |  | [optional]
**status_history** | Option<[**Vec<models::StatusHistoryEntry>**](StatusHistoryEntry.md)> | A chronological list of status transitions the transfer has gone through. | [optional][readonly]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**status_reason** | Option<[**models::StatusReason2**](StatusReason2.md)> |  | [optional]
**metadata** | Option<[**models::Metadata**](Metadata.md)> |  | [optional]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


