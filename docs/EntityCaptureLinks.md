# EntityCaptureLinks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**param_self** | [**models::Url**](url.md) |  | 
**payment** | [**models::Url**](url.md) | The API resource URL of the [payment](get-payment) that this capture belongs to. | 
**settlement** | Option<[**models::UrlNullable**](url-nullable.md)> | The API resource URL of the [settlement](get-settlement) this capture has been settled with. Not present if not yet settled. | [optional]
**shipment** | Option<[**models::UrlNullable**](url-nullable.md)> | The API resource URL of the [shipment](get-shipment) this capture is associated with. Not present if it isn't associated with a shipment. | [optional]
**documentation** | [**models::Url**](url.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


