# \CapabilitiesApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_capabilities**](CapabilitiesApiApi.md#list_capabilities) | **GET** /capabilities | List capabilities



## list_capabilities

> models::ListCapabilities200Response list_capabilities(idempotency_key)
List capabilities

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Retrieve a list of capabilities for an organization.  This API provides detailed insights into the specific requirements and status of each client's onboarding journey.  Capabilities are at the organization level, indicating if the organization can perform a given capability.  For payments, regardless them being at the profile level, the capability is listed at the organization level. This means that if at least one of the clients's profiles can receive payments, the payments capability is enabled, communicating that the organization can indeed receive payments.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListCapabilities200Response**](list_capabilities_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

