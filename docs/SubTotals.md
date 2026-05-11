# SubTotals

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | Option<**i32**> | Number of transactions of this type | [optional]
**method** | Option<[**models::PaymentMethod**](PaymentMethod.md)> | Payment type of the transactions | [optional]
**card_issuer** | Option<[**models::BalanceCardIssuer**](BalanceCardIssuer.md)> | In case of payments transactions with card, the card issuer will be available | [optional]
**card_audience** | Option<[**models::BalanceCardAudience**](BalanceCardAudience.md)> | In case of payments trnsactions with card, the card audience will be available. | [optional]
**card_region** | Option<[**models::BalanceCardRegion**](BalanceCardRegion.md)> | In case of payments transactions with card, the card region will be available. | [optional]
**fee_type** | Option<[**models::BalanceFeeType**](BalanceFeeType.md)> | Present when the transaction represents a fee. | [optional]
**prepayment_part_type** | Option<[**models::BalancePrepaymentPartType**](BalancePrepaymentPartType.md)> | Prepayment part: fee itself, reimbursement, discount, VAT or rounding compensation. | [optional]
**transaction_type** | Option<[**models::BalanceTransactionType**](BalanceTransactionType.md)> | Represents the transaction type | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


