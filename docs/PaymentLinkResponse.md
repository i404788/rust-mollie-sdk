# PaymentLinkResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a payment link object. Will always contain the string `payment-link` for this endpoint. | [optional][readonly]
**id** | Option<**String**> |  | [optional]
**mode** | Option<[**models::Mode**](mode.md)> |  | [optional]
**description** | Option<**String**> | A short description of the payment link. The description is visible in the Dashboard and will be shown on the customer's bank or card statement when possible. | [optional]
**amount** | Option<[**models::AmountNullable**](amount-nullable.md)> | The amount of the payment link. If no amount is provided initially, the customer will be prompted to enter an amount. | [optional]
**minimum_amount** | Option<[**models::AmountNullable**](amount-nullable.md)> | The minimum amount of the payment link. This property is only allowed when there is no amount provided. The customer will be prompted to enter a value greater than or equal to the minimum amount. | [optional]
**archived** | Option<**bool**> | Whether the payment link is archived. Customers will not be able to complete payments on archived payment links. | [optional][readonly]
**redirect_url** | Option<**String**> | The URL your customer will be redirected to after completing the payment process. If no redirect URL is provided, the customer will be shown a generic message after completing the payment. | [optional]
**webhook_url** | Option<**String**> | The webhook URL where we will send payment status updates to.  The webhookUrl is optional, but without a webhook you will miss out on important status changes to any payments resulting from the payment link.  The webhookUrl must be reachable from Mollie's point of view, so you cannot use `localhost`. If you want to use webhook during development on `localhost`, you must use a tool like ngrok to have the webhooks delivered to your local machine. | [optional]
**lines** | Option<[**Vec<models::PaymentLineItemResponse>**](payment-line-item-response.md)> | Optionally provide the order lines for the payment. Each line contains details such as a description of the item ordered and its price.  All lines must have the same currency as the payment.  Required for payment methods `billie`, `in3`, `klarna`, `riverty` and `voucher`. | [optional]
**billing_address** | Option<[**models::PaymentAddress**](payment-address.md)> | The customer's billing address details. We advise to provide these details to improve fraud protection and conversion.  Should include `email` or a valid postal address consisting of `streetAndNumber`, `postalCode`, `city` and `country`.  Required for payment method `in3`, `klarna`, `billie` and `riverty`. | [optional]
**shipping_address** | Option<[**models::PaymentAddress**](payment-address.md)> | The customer's shipping address details. We advise to provide these details to improve fraud protection and conversion.  Should include `email` or a valid postal address consisting of `streetAndNumber`, `postalCode`, `city` and `country`. | [optional]
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) this entity belongs to.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted in the creation request. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. | [optional]
**reusable** | Option<**bool**> | Indicates whether the payment link is reusable. If this field is set to `true`, customers can make multiple payments using the same link.  If no value is specified, the field defaults to `false`, allowing only a single payment per link. | [optional]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**paid_at** | Option<**String**> | The date and time the payment link became paid, in ISO 8601 format. | [optional][readonly]
**expires_at** | Option<**String**> | The date and time the payment link is set to expire, in ISO 8601 format. If no expiry date was provided up front, the payment link will not expire automatically. | [optional]
**allowed_methods** | Option<**Vec<String>**> | An array of payment methods that are allowed to be used for this payment link. When this parameter is not provided or is an empty array, all enabled payment methods will be available.  Enum: 'applepay', 'bancomatpay', 'bancontact', 'banktransfer', 'belfius', 'blik', 'creditcard', 'eps', 'giftcard', 'ideal', 'kbc', 'mybank', 'paybybank', 'paypal', 'paysafecard', 'pointofsale', 'przelewy24', 'satispay', 'trustly', 'twint', 'in3', 'riverty', 'klarna', 'billie'. | [optional]
**application_fee** | Option<[**models::CreatePaymentLinkRequestApplicationFee**](create_payment_link_request_applicationFee.md)> |  | [optional]
**sequence_type** | Option<[**models::PaymentLinkSequenceTypeResponse**](payment-link-sequence-type-response.md)> | If set to `first`, a payment mandate is established right after a payment is made by the customer.  Defaults to `oneoff`, which is a regular payment link and will not establish a mandate after payment.  The mandate ID can be retrieved by making a call to the [Payment Link Payments Endpoint](get-payment-link-payments). | [optional]
**customer_id** | Option<**String**> | **Only relevant when `sequenceType` is set to `first`**  The ID of the [customer](get-customer) the payment link is being created for. If a value is not provided, the customer will be required to input relevant information which will be used to establish a mandate after the payment is made. | [optional]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**_links** | Option<[**models::CreatePaymentLinkRequestLinks**](create_payment_link_request__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


