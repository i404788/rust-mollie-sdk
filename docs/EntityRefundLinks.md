# EntityRefundLinks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**param_self** | [**models::Url**](Url.md) |  | 
**payment** | [**models::Url**](Url.md) | The API resource URL of the [payment](get-payment) that this refund belongs to. | 
**settlement** | Option<[**models::UrlNullable**](UrlNullable.md)> | The API resource URL of the [settlement](get-settlement) this refund has been settled with. Not present if not yet settled. | [optional]
**documentation** | [**models::Url**](Url.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


