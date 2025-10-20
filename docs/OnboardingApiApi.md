# \OnboardingApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_onboarding_status**](OnboardingApiApi.md#get_onboarding_status) | **GET** /onboarding/me | Get onboarding status
[**submit_onboarding_data**](OnboardingApiApi.md#submit_onboarding_data) | **POST** /onboarding/me | Submit onboarding data



## get_onboarding_status

> models::EntityOnboardingStatus get_onboarding_status(idempotency_key)
Get onboarding status

Retrieve the onboarding status of the currently authenticated organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityOnboardingStatus**](entity-onboarding-status.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## submit_onboarding_data

> serde_json::Value submit_onboarding_data(idempotency_key, submit_onboarding_data_request)
Submit onboarding data

**⚠️ We no longer recommend implementing this endpoint. Please refer to the Client Links API instead to kick off the onboarding process for your merchants.**  Submit data that will be prefilled in the merchant's onboarding. The data you submit will only be processed when the onboarding status is `needs-data`.   Information that the merchant has entered in their dashboard will not be overwritten.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**submit_onboarding_data_request** | Option<[**SubmitOnboardingDataRequest**](SubmitOnboardingDataRequest.md)> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

