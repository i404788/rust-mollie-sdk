# RecurringLineItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | Option<**String**> | A description of the recurring item. If not present, the main description of the item will be used. | [optional]
**interval** | **String** | Cadence unit of the recurring item. For example: `12 months`, `52 weeks` or `365 days`.  Possible values: `... days`, `... weeks`, `... months`. | 
**amount** | Option<[**models::Amount**](Amount.md)> | Total amount and currency of the recurring item. | [optional]
**times** | Option<**i32**> | Total number of charges for the subscription to complete. Leave empty for ongoing subscription. | [optional]
**start_date** | Option<**String**> | The start date of the subscription if it does not start right away (format `YYYY-MM-DD`) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


