# EntityRefundLinks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**param_self** | [**models::Url**](url.md) |  | 
**payment** | [**models::Url**](url.md) | The API resource URL of the [payment](get-payment) that this refund belongs to. | 
**settlement** | Option<[**models::UrlNullable**](url-nullable.md)> | The API resource URL of the [settlement](get-settlement) this refund has been settled with. Not present if not yet settled. | [optional]
**documentation** | [**models::Url**](url.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


