# RequestApplePayPaymentSessionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**validation_url** | **String** | The validationUrl you got from the [ApplePayValidateMerchant event](https://developer.apple.com/documentation/apple_pay_on_the_web/applepayvalidatemerchantevent).  A list of all [valid host names](https://developer.apple.com/documentation/apple_pay_on_the_web/setting_up_your_server) for merchant validation is available. You should white list these in your application and reject any `validationUrl`s that have a host name not in the list. | 
**domain** | **String** | The domain of your web shop, that is visible in the browser's location bar. For example `pay.myshop.com`. | 
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) this entity belongs to.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted in the creation request. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


