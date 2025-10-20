# EntityCustomerLinks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**param_self** | [**models::Url**](url.md) |  | 
**dashboard** | [**models::Url**](url.md) |  | 
**payments** | Option<[**models::UrlNullable**](url-nullable.md)> | The API resource URL of the [payments](list-payments) linked to this customer. Omitted if no such payments exist (yet). | [optional]
**mandates** | Option<[**models::UrlNullable**](url-nullable.md)> | The API resource URL of the [mandates](list-mandates) linked to this customer. Omitted if no such mandates exist (yet). | [optional]
**subscriptions** | Option<[**models::UrlNullable**](url-nullable.md)> | The API resource URL of the [subscriptions](list-subscriptions) linked to this customer. Omitted if no such subscriptions exist (yet). | [optional]
**documentation** | [**models::Url**](url.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


