# EntityCaptureResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a capture object. Will always contain the string `capture` for this endpoint. | [optional][readonly]
**id** | Option<**String**> |  | [optional]
**mode** | Option<[**models::Mode**](mode.md)> |  | [optional]
**description** | Option<**String**> | The description of the capture. | [optional]
**amount** | Option<[**models::AmountNullable**](amount-nullable.md)> | The amount captured. If no amount is provided, the full authorized amount is captured. | [optional]
**settlement_amount** | Option<[**models::AmountNullable**](amount-nullable.md)> | This optional field will contain the approximate amount that will be settled to your account, converted to the currency your account is settled in.  Since the field contains an estimated amount during capture processing, it may change over time. To retrieve accurate settlement amounts we recommend using the [List balance transactions endpoint](list-balance-transactions) instead. | [optional][readonly]
**status** | Option<[**models::CaptureStatus**](capture-status.md)> |  | [optional][readonly]
**metadata** | Option<[**models::Metadata**](metadata.md)> |  | [optional]
**payment_id** | Option<**String**> |  | [optional]
**shipment_id** | Option<**String**> |  | [optional]
**settlement_id** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | Option<[**models::EntityCaptureLinks**](entity_capture__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


