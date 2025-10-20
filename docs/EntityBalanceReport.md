# EntityBalanceReport

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a balance report object. Will always contain the string `balance-report` for this endpoint. | [optional][readonly]
**balance_id** | Option<**String**> |  | [optional]
**time_zone** | Option<**String**> | The time zone used for the from and until parameters. Currently only time zone `Europe/Amsterdam` is supported. | [optional]
**from** | Option<**String**> | The start date of the report, in `YYYY-MM-DD` format. The from date is 'inclusive', and in Central European Time. This means a report with for example `from=2024-01-01` will include movements of 2024-01-01 00:00:00 CET and onwards. | [optional]
**until** | Option<**String**> | The end date of the report, in `YYYY-MM-DD` format. The until date is 'exclusive', and in Central European Time. This means a report with for example `until=2024-02-01` will include movements up until 2024-01-31 23:59:59 CET. | [optional]
**grouping** | Option<[**models::BalanceReportGrouping**](balance-report-grouping.md)> |  | [optional]
**totals** | Option<[**models::EntityBalanceReportTotals**](entity_balance_report_totals.md)> |  | [optional]
**_links** | Option<[**models::EntityBalanceLinks**](entity_balance__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


