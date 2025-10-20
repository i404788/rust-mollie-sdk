# EntityOnboardingStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains an onboarding status object. Will always contain the string `onboarding` for this resource type. | [optional][readonly]
**name** | Option<**String**> | The name of the organization. | [optional][readonly]
**status** | Option<[**models::OnboardingStatus**](onboarding-status.md)> |  | [optional][readonly]
**can_receive_payments** | Option<**bool**> | Whether the organization can receive payments. | [optional][readonly]
**can_receive_settlements** | Option<**bool**> | Whether the organization can receive settlements to their external bank account. | [optional][readonly]
**signed_up_at** | Option<**String**> | The sign up date time of the organization in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | Option<[**models::EntityOnboardingStatusLinks**](entity_onboarding_status__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


