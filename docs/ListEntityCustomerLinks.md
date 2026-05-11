# ListEntityCustomerLinks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**param_self** | [**models::Url**](Url.md) |  | 
**dashboard** | [**models::Url**](Url.md) |  | 
**payments** | Option<[**models::UrlNullable**](UrlNullable.md)> | The API resource URL of the [payments](list-payments) linked to this customer. Omitted if no such payments exist (yet). | [optional]
**mandates** | Option<[**models::UrlNullable**](UrlNullable.md)> | The API resource URL of the [mandates](list-mandates) linked to this customer. Omitted if no such mandates exist (yet). | [optional]
**subscriptions** | Option<[**models::UrlNullable**](UrlNullable.md)> | The API resource URL of the [subscriptions](list-subscriptions) linked to this customer. Omitted if no such subscriptions exist (yet). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


