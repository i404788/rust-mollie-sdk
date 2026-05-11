# SessionLineItemResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | Option<[**models::PaymentLineTypeResponse**](PaymentLineTypeResponse.md)> |  | [optional]
**description** | **String** | A description of the line item. For example *LEGO 4440 Forest Police Station*. | 
**quantity** | **i32** | The number of items. | 
**quantity_unit** | Option<**String**> | The unit for the quantity. For example *pcs*, *kg*, or *cm*. | [optional]
**unit_price** | [**models::Amount**](Amount.md) | The price of a single item including VAT.  For example: `{\"currency\":\"EUR\", \"value\":\"89.00\"}` if the box of LEGO costs €89.00 each.  For types `discount`, `store_credit`, and `gift_card`, the unit price must be negative.  The unit price can be zero in case of free items. | 
**discount_amount** | Option<[**models::Amount**](Amount.md)> | Any line-specific discounts, as a positive amount. Not relevant if the line itself is already a discount type. | [optional]
**total_amount** | [**models::Amount**](Amount.md) | The total amount of the line, including VAT and discounts.  Should match the following formula: `(unitPrice × quantity) - discountAmount`.  The sum of all `totalAmount` values of all order lines should be equal to the full payment amount. | 
**vat_rate** | Option<**String**> | The VAT rate applied to the line, for example `21.00` for 21%. The vatRate should be passed as a string and not as a float, to ensure the correct number of decimals are passed. | [optional]
**vat_amount** | Option<[**models::Amount**](Amount.md)> | The amount of value-added tax on the line. The `totalAmount` field includes VAT, so the `vatAmount` can be calculated with the formula `totalAmount × (vatRate / (100 + vatRate))`.  Any deviations from this will result in an error.  For example, for a `totalAmount` of SEK 100.00 with a 25.00% VAT rate, we expect a VAT amount of `SEK 100.00 × (25 / 125) = SEK 20.00`. | [optional]
**sku** | Option<**String**> | The SKU, EAN, ISBN or UPC of the product sold. | [optional]
**image_url** | Option<**String**> | A link pointing to an image of the product sold. | [optional]
**product_url** | Option<**String**> | A link pointing to the product page in your web shop of the product sold. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


