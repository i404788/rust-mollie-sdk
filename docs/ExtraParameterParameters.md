# ExtraParameterParameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**apple_pay_payment_token** | Option<**String**> | The Apple Pay Payment token object (encoded as JSON) that is part of the result of authorizing a payment request. The token contains the payment information needed to authorize the payment.  The object should be passed encoded in a JSON string. | [optional]
**company** | Option<[**models::ExtraParameterParametersCompany**](extra_parameter_parameters_company.md)> |  | [optional]
**card_token** | Option<**String**> | When creating credit card payments using Mollie Components, you need to provide the card token you received from the card component in this field. The token represents the customer's card information needed to complete the payment. Note: field only valid for oneoff and first payments. For recurring payments, the customerId alone is enough. | [optional]
**voucher_number** | Option<**String**> | The card token you received from the card component of Mollie Components. The token represents the customer's card information needed to complete the payment. | [optional]
**voucher_pin** | Option<**String**> | The PIN on the gift card. You can supply this to prefill the PIN, if the card has any. | [optional]
**consumer_date_of_birth** | Option<[**String**](string.md)> | The customer's date of birth. If not provided via the API, iDeal in3 will ask the customer to provide it during the payment process. | [optional]
**extra_merchant_data** | Option<[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)> | For some industries, additional purchase information can be sent to Klarna to increase the authorization rate. You can submit your extra data in this field if you have agreed upon this with Klarna. This field should be an object containing any of the allowed keys and sub-objects described at the Klarna Developer Documentation. | [optional]
**session_id** | Option<**String**> | The unique ID you have used for the PayPal fraud library. You should include this if you use PayPal for an on-demand payment. | [optional]
**digital_goods** | Option<**bool**> | Indicate if you are about to deliver digital goods, such as for example a software license. Setting this parameter can have consequences for your PayPal Seller Protection. Refer to PayPal's documentation for more information. | [optional]
**customer_reference** | Option<**String**> | Used by paysafecard for customer identification across payments. When you generate a customer reference yourself, make sure not to put personal identifiable information or IP addresses in the customer reference directly. | [optional]
**terminal_id** | Option<**String**> | The ID of the terminal device where you want to initiate the payment on. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


