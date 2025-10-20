# UpdatePaymentLinkRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | Option<**String**> | A short description of the payment link. The description is visible in the Dashboard and will be shown on the customer's bank or card statement when possible.  Updating the description does not affect any previously existing payments created for this payment link. | [optional]
**minimum_amount** | Option<[**models::Amount**](amount.md)> | The minimum amount of the payment link. This property is only allowed when there is no amount provided. The customer will be prompted to enter a value greater than or equal to the minimum amount. | [optional]
**archived** | Option<**bool**> | Whether the payment link is archived. Customers will not be able to complete payments on archived payment links. | [optional]
**allowed_methods** | Option<**Vec<String>**> | An array of payment methods that are allowed to be used for this payment link. When this parameter is not provided or is an empty array, all enabled payment methods will be available.  Enum: 'applepay', 'bancomatpay', 'bancontact', 'banktransfer', 'belfius', 'blik', 'creditcard', 'eps', 'giftcard', 'ideal', 'kbc', 'mybank', 'paybybank', 'paypal', 'paysafecard', 'pointofsale', 'przelewy24', 'satispay', 'trustly', 'twint', 'in3', 'riverty', 'klarna', 'billie'. | [optional]
**lines** | Option<[**Vec<models::PaymentLineItem>**](payment-line-item.md)> | Optionally provide the order lines for the payment. Each line contains details such as a description of the item ordered and its price.  All lines must have the same currency as the payment.  Required for payment methods `billie`, `in3`, `klarna`, `riverty` and `voucher`. | [optional]
**billing_address** | Option<[**models::PaymentAddress**](payment-address.md)> | The customer's billing address details. We advise to provide these details to improve fraud protection and conversion.  Should include `email` or a valid postal address consisting of `streetAndNumber`, `postalCode`, `city` and `country`.  Required for payment method `in3`, `klarna`, `billie` and `riverty`. | [optional]
**shipping_address** | Option<[**models::PaymentAddress**](payment-address.md)> | The customer's shipping address details. We advise to provide these details to improve fraud protection and conversion.  Should include `email` or a valid postal address consisting of `streetAndNumber`, `postalCode`, `city` and `country`. | [optional]
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


