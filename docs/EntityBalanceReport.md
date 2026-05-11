# EntityBalanceReport

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a balance report object. Will always contain the string `balance-report` for this endpoint. | [readonly]
**balance_id** | **String** | The ID of the balance this report is generated for. | 
**time_zone** | **String** | The time zone used for the from and until parameters. Currently only time zone `Europe/Amsterdam` is supported. | 
**from** | **String** | The start date of the report, in `YYYY-MM-DD` format. The from date is 'inclusive', and in Central European Time. This means a report with for example `from=2024-01-01` will include movements of 2024-01-01 00:00:00 CET and onwards. | 
**until** | **String** | The end date of the report, in `YYYY-MM-DD` format. The until date is 'exclusive', and in Central European Time. This means a report with for example `until=2024-02-01` will include movements up until 2024-01-31 23:59:59 CET. | 
**grouping** | [**models::BalanceReportGrouping**](BalanceReportGrouping.md) |  | 
**totals** | [**models::EntityBalanceReportTotals**](EntityBalanceReportTotals.md) |  | 
**_links** | [**models::EntityBalanceLinks**](EntityBalanceLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


