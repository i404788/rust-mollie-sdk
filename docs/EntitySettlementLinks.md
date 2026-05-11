# EntitySettlementLinks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**param_self** | [**models::Url**](Url.md) |  | 
**payments** | Option<[**models::Url**](Url.md)> | The API resource URL of the [payments](list-payments) included in this settlement. | [optional]
**captures** | Option<[**models::Url**](Url.md)> | The API resource URL of the [captures](list-captures) included in this settlement. | [optional]
**refunds** | Option<[**models::Url**](Url.md)> | The API resource URL of the [refunds](list-refunds) deducted from this settlement. | [optional]
**chargebacks** | Option<[**models::Url**](Url.md)> | The API resource URL of the [chargebacks](list-chargebacks) deducted from this settlement. | [optional]
**invoice** | Option<[**models::UrlNullable**](UrlNullable.md)> | The API resource URL of the [invoice](list-invoices). | [optional]
**documentation** | Option<[**models::Url**](Url.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


