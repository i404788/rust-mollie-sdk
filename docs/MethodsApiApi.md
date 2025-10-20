# \MethodsApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**disable_method**](MethodsApiApi.md#disable_method) | **DELETE** /profiles/{profileId}/methods/{id} | Disable payment method
[**disable_method_issuer**](MethodsApiApi.md#disable_method_issuer) | **DELETE** /profiles/{profileId}/methods/{methodId}/issuers/{id} | Disable payment method issuer
[**enable_method**](MethodsApiApi.md#enable_method) | **POST** /profiles/{profileId}/methods/{id} | Enable payment method
[**enable_method_issuer**](MethodsApiApi.md#enable_method_issuer) | **POST** /profiles/{profileId}/methods/{methodId}/issuers/{id} | Enable payment method issuer
[**get_method**](MethodsApiApi.md#get_method) | **GET** /methods/{id} | Get payment method
[**list_all_methods**](MethodsApiApi.md#list_all_methods) | **GET** /methods/all | List all payment methods
[**list_methods**](MethodsApiApi.md#list_methods) | **GET** /methods | List payment methods



## disable_method

> serde_json::Value disable_method(profile_id, id, idempotency_key)
Disable payment method

Disable a payment method on a specific profile.  When using a profile-specific API credential, the alias `me` can be used instead of the profile ID to refer to the current profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Provide the ID of the related profile. | [required] |
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## disable_method_issuer

> serde_json::Value disable_method_issuer(profile_id, method_id, id, idempotency_key)
Disable payment method issuer

Disable an issuer for a payment method on a specific profile.  Currently only the payment methods `voucher` and `giftcard` are supported.  When using a profile-specific API credential, the alias `me` can be used instead of the profile ID to refer to the current profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Provide the ID of the related profile. | [required] |
**method_id** | **String** | Provide the ID of the related payment method. | [required] |
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enable_method

> models::EntityMethod enable_method(profile_id, id, idempotency_key)
Enable payment method

Enable a payment method on a specific profile.  When using a profile-specific API credential, the alias `me` can be used instead of the profile ID to refer to the current profile.  Some payment methods require extra steps in order to be activated. In cases where a step at the payment method provider needs to be completed first, the status will be set to `pending-external` and the response will contain a link to complete the activation at the provider.  To enable voucher or gift card issuers, refer to the [Enable payment method issuer](enable-method-issuer) endpoint.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Provide the ID of the related profile. | [required] |
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityMethod**](entity-method.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enable_method_issuer

> models::EnableMethodIssuer200Response enable_method_issuer(profile_id, method_id, id, idempotency_key, enable_method_issuer_request)
Enable payment method issuer

Enable an issuer for a payment method on a specific profile.  Currently only the payment methods `voucher` and `giftcard` are supported.  When using a profile-specific API credential, the alias `me` can be used instead of the profile ID to refer to the current profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Provide the ID of the related profile. | [required] |
**method_id** | **String** | Provide the ID of the related payment method. | [required] |
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**enable_method_issuer_request** | Option<[**EnableMethodIssuerRequest**](EnableMethodIssuerRequest.md)> |  |  |

### Return type

[**models::EnableMethodIssuer200Response**](enable_method_issuer_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_method

> models::EntityMethod get_method(id, locale, currency, profile_id, include, sequence_type, testmode, idempotency_key)
Get payment method

Retrieve a single payment method by its ID.  If a method is not available on this profile, a `404 Not Found` response is returned. If the method is available but not enabled yet, a status `403 Forbidden` is returned. You can enable payments methods via the [Enable payment method endpoint](enable-method) of the Profiles API, or via the Mollie Dashboard.  If you do not know the method's ID, you can use the [methods list endpoint](list-methods) to retrieve all payment methods that are available.  Additionally, it is possible to check if wallet methods such as Apple Pay are enabled by passing the wallet ID (`applepay`) as the method ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**locale** | Option<**String**> | Response language |  |
**currency** | Option<**String**> | If provided, the `minimumAmount` and `maximumAmount` will be converted to the given currency. An error is returned if the currency is not supported by the payment method. |  |
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) you wish to retrieve the resources for.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. |  |
**include** | Option<**String**> | This endpoint allows you to include additional information via the `include` query string parameter. |  |
**sequence_type** | Option<[**SequenceType**](.md)> | Set this parameter to `first` to only return the methods that can be used for the first payment of a recurring sequence.  Set it to `recurring` to only return methods that can be used for recurring payments or subscriptions. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityMethod**](entity-method.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_all_methods

> models::ListAllMethods200Response list_all_methods(locale, amount, include, sequence_type, profile_id, testmode, idempotency_key)
List all payment methods

Retrieve all payment methods that Mollie offers, regardless of the eligibility of the organization for the specific method. The results of this endpoint are **not** paginated — unlike most other list endpoints in our API.  The list can optionally be filtered using a number of parameters described below.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**locale** | Option<**String**> | Response language |  |
**amount** | Option<[**Amount**](.md)> | If supplied, only payment methods that support the amount and currency are returned.  Example: `/v2/methods/all?amount[value]=100.00&amount[currency]=USD` |  |
**include** | Option<**String**> | This endpoint allows you to include additional information via the `include` query string parameter. |  |
**sequence_type** | Option<[**SequenceType**](.md)> | Set this parameter to `first` to only return the methods that can be used for the first payment of a recurring sequence.  Set it to `recurring` to only return methods that can be used for recurring payments or subscriptions. |  |
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) you wish to retrieve the resources for.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListAllMethods200Response**](list_all_methods_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_methods

> models::ListMethods200Response list_methods(sequence_type, locale, amount, resource, billing_country, include_wallets, order_line_categories, profile_id, include, testmode, idempotency_key)
List payment methods

Retrieve all enabled payment methods. The results of this endpoint are **not** paginated — unlike most other list endpoints in our API.  For test mode, all pending and enabled payment methods are returned. If no payment methods are requested yet, the most popular payment methods are returned in the test mode. For live mode, only fully enabled payment methods are returned.  Payment methods can be requested and enabled via the Mollie Dashboard, or via the [Enable payment method endpoint](enable-method) of the Profiles API.  The list can optionally be filtered using a number of parameters described below.  By default, only payment methods for the Euro currency are returned. If you wish to retrieve payment methods which exclusively support other currencies (e.g. Twint), you need to use the `amount` parameters.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_type** | Option<[**SequenceType**](.md)> | Set this parameter to `first` to only return the enabled methods that can be used for the first payment of a recurring sequence.  Set it to `recurring` to only return enabled methods that can be used for recurring payments or subscriptions. |  |
**locale** | Option<**String**> | Response language |  |
**amount** | Option<[**Amount**](.md)> | If supplied, only payment methods that support the amount and currency are returned.  Example: `/v2/methods?amount[value]=100.00&amount[currency]=USD` |  |
**resource** | Option<**String**> | **⚠️ We no longer recommend using the Orders API. Please refer to the [Payments API](payments-api) instead.**  Indicate if you will use the result for the [Create order](create-order) or the [Create payment](create-payment) endpoint.  When passing the value `orders`, the result will include payment methods that are only available for payments created via the Orders API. |  |
**billing_country** | Option<**String**> | The country taken from your customer's billing address in ISO 3166-1 alpha-2 format. This parameter can be used to check whether your customer is eligible for certain payment methods, for example for Klarna.  Example: `/v2/methods?resource=orders&billingCountry=DE` |  |
**include_wallets** | Option<**String**> | A comma-separated list of the wallets you support in your checkout. Wallets often require wallet specific code to check if they are available on the shoppers device, hence the need to indicate your support. |  |
**order_line_categories** | Option<[**LineCategories**](.md)> | A comma-separated list of the line categories you support in your checkout.  Example: `/v2/methods?orderLineCategories=eco,meal` |  |
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) you wish to retrieve the resources for.  Most API credentials are linked to a single profile. In these cases the `profileId` can be omitted. For organization-level credentials such as OAuth access tokens however, the `profileId` parameter is required. |  |
**include** | Option<**String**> | This endpoint allows you to include additional information via the `include` query string parameter. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListMethods200Response**](list_methods_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

