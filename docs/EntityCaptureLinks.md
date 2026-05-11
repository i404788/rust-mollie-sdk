# EntityCaptureLinks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**param_self** | [**models::Url**](Url.md) |  | 
**payment** | [**models::Url**](Url.md) | The API resource URL of the [payment](get-payment) that this capture belongs to. | 
**settlement** | Option<[**models::UrlNullable**](UrlNullable.md)> | The API resource URL of the [settlement](get-settlement) this capture has been settled with. Not present if not yet settled. | [optional]
**shipment** | Option<[**models::UrlNullable**](UrlNullable.md)> | The API resource URL of the [shipment](get-shipment) this capture is associated with. Not present if it isn't associated with a shipment. | [optional]
**documentation** | [**models::Url**](Url.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


