# \ProfilesApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_profile**](ProfilesApiApi.md#create_profile) | **POST** /profiles | Create profile
[**delete_profile**](ProfilesApiApi.md#delete_profile) | **DELETE** /profiles/{id} | Delete profile
[**get_current_profile**](ProfilesApiApi.md#get_current_profile) | **GET** /profiles/me | Get current profile
[**get_profile**](ProfilesApiApi.md#get_profile) | **GET** /profiles/{id} | Get profile
[**list_profiles**](ProfilesApiApi.md#list_profiles) | **GET** /profiles | List profiles
[**update_profile**](ProfilesApiApi.md#update_profile) | **PATCH** /profiles/{id} | Update profile



## create_profile

> models::EntityProfileResponse create_profile(entity_profile, idempotency_key)
Create profile

Create a profile to process payments on.  Profiles are required for payment processing. Normally they are created via the Mollie dashboard. Alternatively, you can use this endpoint to automate profile creation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**entity_profile** | [**EntityProfile**](EntityProfile.md) |  | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityProfileResponse**](entity-profile-response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_profile

> serde_json::Value delete_profile(id, idempotency_key)
Delete profile

Delete a profile. A deleted profile and its related credentials can no longer be used for accepting payments.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_current_profile

> models::EntityProfileResponse get_current_profile(idempotency_key)
Get current profile

Retrieve the currently authenticated profile. A convenient alias of the [Get profile](get-profile) endpoint.  For a complete reference of the profile object, refer to the [Get profile](get-profile) endpoint documentation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityProfileResponse**](entity-profile-response.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_profile

> models::EntityProfileResponse get_profile(id, testmode, idempotency_key)
Get profile

Retrieve a single profile by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityProfileResponse**](entity-profile-response.md)

### Authorization

[oAuth](../README.md#oAuth)

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

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_profile

> models::EntityProfileResponse update_profile(id, update_profile_request, idempotency_key)
Update profile

Update an existing profile.  Profiles are required for payment processing. Normally they are created and updated via the Mollie dashboard. Alternatively, you can use this endpoint to automate profile management.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**update_profile_request** | [**UpdateProfileRequest**](UpdateProfileRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityProfileResponse**](entity-profile-response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

