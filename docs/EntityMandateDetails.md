# EntityMandateDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**consumer_name** | Option<**String**> | The customer's name. Available for SEPA Direct Debit and PayPal mandates. | [optional]
**consumer_account** | Option<**String**> | The customer's IBAN or email address. Available for SEPA Direct Debit and PayPal mandates. | [optional]
**consumer_bic** | Option<**String**> | The BIC of the customer's bank. Available for SEPA Direct Debit mandates. | [optional]
**card_holder** | Option<**String**> | The card holder's name. Available for card mandates. | [optional]
**card_number** | Option<**String**> | The last four digits of the card number. Available for card mandates. | [optional]
**card_expiry_date** | Option<**String**> | The card's expiry date in `YYYY-MM-DD` format. Available for card mandates. | [optional]
**card_label** | Option<[**models::MandateDetailsCardLabel**](MandateDetailsCardLabel.md)> |  | [optional]
**card_fingerprint** | Option<**String**> | Unique alphanumeric representation of this specific card. Available for card mandates. Can be used to identify returning customers. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


