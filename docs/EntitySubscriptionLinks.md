# EntitySubscriptionLinks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**param_self** | [**models::Url**](Url.md) |  | 
**customer** | [**models::UrlNullable**](UrlNullable.md) | The API resource URL of the [customer](get-customer) this subscription was created for. | 
**mandate** | Option<[**models::UrlNullable**](UrlNullable.md)> | The API resource URL of the [mandate](get-mandate) this subscription was created for. | [optional]
**profile** | [**models::UrlNullable**](UrlNullable.md) | The API resource URL of the [profile](get-profile) this subscription was created for. | 
**payments** | Option<[**models::UrlNullable**](UrlNullable.md)> | The API resource URL of the [payments](list-payments) created for this subscription. Omitted if no such payments exist (yet). | [optional]
**documentation** | [**models::Url**](Url.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


