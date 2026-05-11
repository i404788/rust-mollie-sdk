# UpdateSubscriptionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | Option<[**models::Amount**](Amount.md)> | Update the amount for future payments of this subscription. | [optional]
**description** | Option<**String**> | The subscription's description will be used as the description of the resulting individual payments and so showing up on the bank statement of the consumer.  **Please note:** the description needs to be unique for the Customer in case it has multiple active subscriptions. | [optional]
**interval** | Option<**String**> | Interval to wait between payments, for example `1 month` or `14 days`.  The maximum interval is one year (`12 months`, `52 weeks`, or `365 days`).  Possible values: `... days`, `... weeks`, `... months`. | [optional]
**start_date** | Option<**String**> | The start date of the subscription in `YYYY-MM-DD` format. | [optional]
**times** | Option<**i32**> | Total number of payments for the subscription. Once this number of payments is reached, the subscription is considered completed.  Test mode subscriptions will get canceled automatically after 10 payments. | [optional]
**metadata** | Option<[**models::Metadata**](Metadata.md)> | Provide any data you like, for example a string or a JSON object. We will save the data alongside the entity. Whenever you fetch the entity with our API, we will also include the metadata. You can use up to approximately 1kB.  Any metadata added to the subscription will be automatically forwarded to the payments generated for it. | [optional]
**webhook_url** | Option<**String**> | We will call this URL for any payment status changes of payments resulting from this subscription.  This webhook will receive **all** events for the subscription's payments. This may include payment failures as well. Be sure to verify the payment's subscription ID and its status. | [optional]
**mandate_id** | Option<**String**> | The mandate used for this subscription, if any. | [optional]
**testmode** | Option<**bool**> | Whether the entity was created in test mode or live mode. This field does not update the mode of the entity.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


