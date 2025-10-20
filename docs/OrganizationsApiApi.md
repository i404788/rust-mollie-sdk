# \OrganizationsApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_current_organization**](OrganizationsApiApi.md#get_current_organization) | **GET** /organizations/me | Get current organization
[**get_organization**](OrganizationsApiApi.md#get_organization) | **GET** /organizations/{id} | Get organization
[**get_partner_status**](OrganizationsApiApi.md#get_partner_status) | **GET** /organizations/me/partner | Get partner status



## get_current_organization

> models::EntityOrganization get_current_organization(idempotency_key)
Get current organization

Retrieve the currently authenticated organization. A convenient alias of the [Get organization](get-organization) endpoint.  For a complete reference of the organization object, refer to the [Get organization](get-organization) endpoint documentation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityOrganization**](entity-organization.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_organization

> models::EntityOrganization get_organization(id, testmode, idempotency_key)
Get organization

Retrieve a single organization by its ID.  You can normally only retrieve the currently authenticated organization with this endpoint. This is primarily useful for OAuth apps. See also [Get current organization](get-current-organization).  If you have a *partner account*', you can retrieve organization details of connected organizations.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityOrganization**](entity-organization.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_partner_status

> models::GetPartnerStatus200Response get_partner_status(idempotency_key)
Get partner status

Retrieve partnership details about the currently authenticated organization. Only relevant for so-called *partner accounts*.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::GetPartnerStatus200Response**](get_partner_status_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

