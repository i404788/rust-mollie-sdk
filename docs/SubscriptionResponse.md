# SubscriptionResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a subscription object. Will always contain the string `subscription` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this subscription. Example: `sub_rVKGtNd6s3`. | [readonly]
**mode** | [**models::Mode**](Mode.md) |  | 
**status** | [**models::SubscriptionStatusResponse**](SubscriptionStatusResponse.md) |  | [readonly]
**amount** | [**models::Amount**](Amount.md) | The amount for each individual payment that is charged with this subscription. For example, for a monthly subscription of €10, the subscription amount should be set to €10. | 
**times** | **i32** | Total number of payments for the subscription. Once this number of payments is reached, the subscription is considered completed.  Test mode subscriptions will get canceled automatically after 10 payments. | 
**times_remaining** | **i32** | Number of payments left for the subscription. | [readonly]
**interval** | **String** | Interval to wait between payments, for example `1 month` or `14 days`.  The maximum interval is one year (`12 months`, `52 weeks`, or `365 days`).  Possible values: `... days`, `... weeks`, `... months`. | 
**start_date** | **String** | The start date of the subscription in `YYYY-MM-DD` format. | 
**next_payment_date** | Option<**String**> | The date of the next scheduled payment in `YYYY-MM-DD` format. If the subscription has been completed or canceled, this parameter will not be returned. | [optional][readonly]
**description** | **String** | The subscription's description will be used as the description of the resulting individual payments and so showing up on the bank statement of the consumer.  **Please note:** the description needs to be unique for the Customer in case it has multiple active subscriptions. | 
**method** | Option<[**models::SubscriptionMethodResponse**](SubscriptionMethodResponse.md)> |  | 
**application_fee** | Option<[**models::EntitySubscriptionApplicationFee**](EntitySubscriptionApplicationFee.md)> |  | [optional]
**metadata** | Option<[**models::Metadata**](Metadata.md)> | Provide any data you like, for example a string or a JSON object. We will save the data alongside the entity. Whenever you fetch the entity with our API, we will also include the metadata. You can use up to approximately 1kB.  Any metadata added to the subscription will be automatically forwarded to the payments generated for it. | 
**webhook_url** | **String** | We will call this URL for any payment status changes of payments resulting from this subscription.  This webhook will receive **all** events for the subscription's payments. This may include payment failures as well. Be sure to verify the payment's subscription ID and its status. | 
**customer_id** | **String** | The customer this subscription belongs to. | [readonly]
**mandate_id** | Option<**String**> | The mandate used for this subscription, if any. | [optional]
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**canceled_at** | Option<**String**> | The subscription's date and time of cancellation, in ISO 8601 format. This parameter is omitted if the subscription is not canceled (yet). | [optional][readonly]
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) this entity belongs to.  When using an API Key, the `profileId` must not be sent since it is linked to the key. However, for OAuth and Organization tokens, the `profileId` is required.  For more information, see [Authentication](authentication). | [optional]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**_links** | [**models::EntitySubscriptionLinks**](EntitySubscriptionLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


