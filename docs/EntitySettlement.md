# EntitySettlement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a settlement object. Will always contain the string `settlement` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this settlement. | [readonly]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**reference** | Option<**String**> | The settlement's bank reference, as found in your Mollie account and on your bank statement. | [optional][readonly]
**settled_at** | Option<**String**> | The date on which the settlement was settled, in ISO 8601 format.  For an [open settlement](get-open-settlement) or for the [next settlement](get-next-settlement), no settlement date is available. | [optional][readonly]
**status** | [**models::SettlementStatus**](SettlementStatus.md) |  | [readonly]
**amount** | [**models::Amount**](Amount.md) | The total amount of the settlement. | [readonly]
**balance_id** | **String** | The balance token that the settlement was settled to. | [readonly]
**invoice_id** | Option<**String**> | The ID of the oldest invoice created for all the periods, if the invoice has been created yet. | [optional][readonly]
**periods** | Option<**std::collections::HashMap<String, std::collections::HashMap<String, models::EntitySettlementPeriodsValueValue>>**> | For bookkeeping purposes, the settlement includes an overview of transactions included in the settlement. These transactions are grouped into 'period' objects — one for each calendar month.  For example, if a settlement includes funds from 15 April until 4 May, it will include two period objects. One for all transactions processed between 15 April and 30 April, and one for all transactions between 1 May and 4 May.  Period objects are grouped by year, and then by month. So in the above example, the full `periods` collection will look as follows: `{\"2024\": {\"04\": {...}, \"05\": {...}}}`. The year and month in this documentation are referred as `<year>` and `<month>`.  The example response should give a good idea of what this looks like in practise. | [optional][readonly]
**_links** | [**models::EntitySettlementLinks**](EntitySettlementLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


