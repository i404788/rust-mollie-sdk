# EntityPaymentLinks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**param_self** | [**models::Url**](Url.md) |  | 
**checkout** | Option<[**models::Url**](Url.md)> | The URL your customer should visit to make the payment. This is where you should redirect the customer to. | [optional]
**mobile_app_checkout** | Option<[**models::Url**](Url.md)> | The deeplink URL to the app of the payment method. Currently only available for `bancontact`. | [optional]
**change_payment_state** | Option<[**models::UrlNullable**](UrlNullable.md)> | For test mode payments in certain scenarios, a hosted interface is available to help you test different payment states.  Firstly, for recurring test mode payments. Recurring payments do not have a checkout URL, because these payments are executed without any user interaction.  Secondly, for paid test mode payments. The payment state screen will then allow you to create a refund or chargeback for the test payment. | [optional]
**dashboard** | [**models::Url**](Url.md) | Direct link to the payment in the Mollie Dashboard. | 
**refunds** | Option<[**models::Url**](Url.md)> | The API resource URL of the [refunds](list-payment-refunds) that belong to this payment. | [optional]
**chargebacks** | Option<[**models::Url**](Url.md)> | The API resource URL of the [chargebacks](list-payment-chargebacks) that belong to this payment. | [optional]
**captures** | Option<[**models::Url**](Url.md)> | The API resource URL of the [captures](list-payment-captures) that belong to this payment. | [optional]
**settlement** | Option<[**models::Url**](Url.md)> | The API resource URL of the [settlement](get-settlement) this payment has been settled with. Not present if not yet settled. | [optional]
**customer** | Option<[**models::Url**](Url.md)> | The API resource URL of the [customer](get-customer). | [optional]
**mandate** | Option<[**models::Url**](Url.md)> | The API resource URL of the [mandate](get-mandate). | [optional]
**subscription** | Option<[**models::Url**](Url.md)> | The API resource URL of the [subscription](get-subscription). | [optional]
**order** | Option<[**models::Url**](Url.md)> | The API resource URL of the [order](get-order) this payment was created for. Not present if not created for an order. | [optional]
**terminal** | Option<[**models::Url**](Url.md)> | The API resource URL of the [terminal](get-terminal) this payment was created for. Only present for point-of-sale payments. | [optional]
**documentation** | Option<[**models::Url**](Url.md)> |  | [optional]
**status** | Option<[**models::Url**](Url.md)> | Link to customer-facing page showing the status of the bank transfer (to verify if the transaction was successful). | [optional]
**pay_online** | Option<[**models::Url**](Url.md)> | Link to Mollie Checkout page allowing customers to select a different payment method instead of legacy bank transfer. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


