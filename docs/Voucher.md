# Voucher

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a payment method issuer object. Will always contain the string `issuer` for this endpoint. | [readonly]
**id** | **String** | The unique identifier of the payment method issuer. | [readonly]
**name** | **String** | The full name of the payment method issuer. | [readonly]
**image** | [**models::VoucherImage**](voucher_image.md) |  | 
**status** | [**models::MethodIssuerStatus**](method-issuer-status.md) |  | [readonly]
**contractor** | [**models::VoucherContractor**](voucher_contractor.md) |  | 
**_links** | [**models::EntityBalanceLinks**](entity_balance__links.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


