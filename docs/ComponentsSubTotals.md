# ComponentsSubTotals

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sub_totals** | Option<[**Vec<models::SubTotals>**](sub-totals.md)> |  | [optional]
**count** | Option<**i32**> | Number of transactions of this type | [optional]
**method** | Option<[**models::PaymentMethod**](payment-method.md)> | Payment type of the transactions | [optional]
**card_issuer** | Option<**String**> | In case of payments transactions with card, the card issuer will be available | [optional]
**card_audience** | Option<**String**> | In case of payments trnsactions with card, the card audience will be available. | [optional]
**card_region** | Option<**String**> | In case of payments transactions with card, the card region will be available. | [optional]
**fee_type** | Option<**String**> | Present when the transaction represents a fee. | [optional]
**prepayment_part_type** | Option<**String**> | Prepayment part: fee itself, reimbursement, discount, VAT or rounding compensation. | [optional]
**transaction_type** | Option<**String**> | Represents the transaction type | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


