# EntityMethod

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a payment method object. Will always contain the string `method` for this endpoint. | [readonly]
**id** | Option<[**models::MethodResponse**](method-response.md)> | The unique identifier of the payment method. When used during [payment creation](create-payment), the payment method selection screen will be skipped. | [readonly]
**description** | **String** | The full name of the payment method.  If a `locale` parameter is provided, the name is translated to the given locale if possible. | [readonly]
**minimum_amount** | [**models::Amount**](amount.md) | The minimum payment amount required to use this payment method. | [readonly]
**maximum_amount** | [**models::AmountNullable**](amount-nullable.md) | The maximum payment amount allowed when using this payment method. If there is no method-specific maximum, `null` is returned instead. | [readonly]
**image** | [**models::EntityMethodImage**](entity_method_image.md) |  | 
**status** | [**models::MethodStatus**](method-status.md) |  | 
**issuers** | Option<[**Vec<models::EntityMethodIssuersInner>**](entity_method_issuers_inner.md)> | **Optional include.** Array of objects for each 'issuer' that is available for this payment method. Only relevant for iDEAL, KBC/CBC, gift cards, and vouchers. | [optional]
**_links** | [**models::EntityMethodLinks**](entity_method__links.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


