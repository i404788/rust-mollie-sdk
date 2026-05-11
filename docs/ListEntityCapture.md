# ListEntityCapture

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a capture object. Will always contain the string `capture` for this endpoint. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this capture. Example: `cpt_mNepDkEtco6ah3QNPUGYH`. | [optional][readonly]
**mode** | Option<[**models::Mode**](Mode.md)> |  | [optional]
**description** | Option<**String**> | The description of the capture. | [optional]
**amount** | Option<[**models::AmountNullable**](AmountNullable.md)> | The amount captured. If no amount is provided, the full authorized amount is captured. | [optional]
**settlement_amount** | Option<[**models::AmountNullable**](AmountNullable.md)> | **Deprecated.** This field will be removed on January 1st, 2027. Use the [Settlements API](list-settlements) or the [List balance transactions endpoint](list-balance-transactions) for settlement data.  The amount that will be settled to your account for this capture, converted to the currency your account is settled in. Only available once the capture is finalized and the final settlement amount has been determined. | [optional][readonly]
**status** | Option<[**models::CaptureStatusResponse**](CaptureStatusResponse.md)> |  | [optional][readonly]
**metadata** | Option<[**models::Metadata**](Metadata.md)> |  | [optional]
**payment_id** | Option<**String**> | The unique identifier of the payment this capture was created for. For example: `tr_5B8cwPMGnU6qLbRvo7qEZo`. The full payment object can be retrieved via the payment URL in the `_links` object. | [optional][readonly]
**shipment_id** | Option<**String**> | The unique identifier of the shipment that triggered the creation of this capture, if applicable. For example: `shp_gNapNy9qQTUFZYnCrCF7J`. | [optional][readonly]
**settlement_id** | Option<**String**> | The identifier referring to the settlement this capture was settled with. For example, `stl_BkEjN2eBb`. This field is omitted if the capture is not settled (yet). | [optional][readonly]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | Option<[**models::ListEntityCaptureLinks**](ListEntityCaptureLinks.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


