# EntityPaymentResponseDetailsReceipt

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authorization_code** | Option<**String**> | A unique code provided by the cardholder’s bank to confirm that the transaction was successfully approved. | [optional]
**application_identifier** | Option<**String**> | The unique number that identifies a specific payment application on a chip card. | [optional]
**card_read_method** | Option<[**models::PaymentDetailsReceiptCardReadMethodResponse**](payment-details-receipt-card-read-method-response.md)> |  | [optional]
**card_verification_method** | Option<[**models::PaymentDetailsReceiptCardVerificationMethodResponse**](payment-details-receipt-card-verification-method-response.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


