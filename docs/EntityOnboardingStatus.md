# EntityOnboardingStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains an onboarding status object. Will always contain the string `onboarding` for this resource type. | [readonly]
**name** | **String** | The name of the organization. | [readonly]
**status** | [**models::OnboardingStatus**](OnboardingStatus.md) |  | [readonly]
**can_receive_payments** | **bool** | Whether the organization can receive payments. | [readonly]
**can_receive_settlements** | **bool** | Whether the organization can receive settlements to their external bank account. | [readonly]
**signed_up_at** | **String** | The sign up date time of the organization in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]
**_links** | [**models::EntityOnboardingStatusLinks**](EntityOnboardingStatusLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


