# \ProfilesApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_profile**](ProfilesApiApi.md#create_profile) | **POST** /v2/profiles | Create profile
[**delete_profile**](ProfilesApiApi.md#delete_profile) | **DELETE** /v2/profiles/{profileId} | Delete profile
[**get_current_profile**](ProfilesApiApi.md#get_current_profile) | **GET** /v2/profiles/me | Get current profile
[**get_profile**](ProfilesApiApi.md#get_profile) | **GET** /v2/profiles/{profileId} | Get profile
[**list_profiles**](ProfilesApiApi.md#list_profiles) | **GET** /v2/profiles | List profiles
[**update_profile**](ProfilesApiApi.md#update_profile) | **PATCH** /v2/profiles/{profileId} | Update profile



## create_profile

> models::ProfileResponse create_profile(profile_request, idempotency_key)
Create profile

Create a profile to process payments on.  Profiles are required for payment processing. Normally they are created via the Mollie dashboard. Alternatively, you can use this endpoint to automate profile creation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_request** | [**ProfileRequest**](ProfileRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ProfileResponse**](profile-response.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_profile

> delete_profile(profile_id, idempotency_key)
Delete profile

Delete a profile. A deleted profile and its related credentials can no longer be used for accepting payments.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Provide the ID of the related profile. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

 (empty response body)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_current_profile

> models::ProfileResponse get_current_profile(idempotency_key)
Get current profile

Retrieve the currently authenticated profile. A convenient alias of the [Get profile](get-profile) endpoint.  For a complete reference of the profile object, refer to the [Get profile](get-profile) endpoint documentation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ProfileResponse**](profile-response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_profile

> models::ProfileResponse get_profile(profile_id, testmode, idempotency_key)
Get profile

Retrieve a single profile by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Provide the ID of the related profile. | [required] |
**testmode** | Option<**bool**> | You can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ProfileResponse**](profile-response.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_profiles

> models::ListProfiles200Response list_profiles(from, limit, idempotency_key)
List profiles

Retrieve a list of all of your profiles.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListProfiles200Response**](list_profiles_200_response.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_profile

> models::ProfileResponse update_profile(profile_id, update_profile_request, idempotency_key)
Update profile

Update an existing profile.  Profiles are required for payment processing. Normally they are created and updated via the Mollie dashboard. Alternatively, you can use this endpoint to automate profile management.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Provide the ID of the related profile. | [required] |
**update_profile_request** | [**UpdateProfileRequest**](UpdateProfileRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ProfileResponse**](profile-response.md)

### Authorization

[oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

