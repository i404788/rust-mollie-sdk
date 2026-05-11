# \OAuthApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**oauth_generate_tokens**](OAuthApiApi.md#oauth_generate_tokens) | **POST** /oauth2/tokens | Generate tokens
[**oauth_revoke_tokens**](OAuthApiApi.md#oauth_revoke_tokens) | **DELETE** /oauth2/tokens | Revoke tokens



## oauth_generate_tokens

> models::OauthGenerateTokens200Response oauth_generate_tokens(authorization, content_type, idempotency_key, oauth_generate_tokens_request)
Generate tokens

Exchange the authorization code you received from the [Authorize endpoint](oauth-authorize) for an 'access token' API credential, with which you can communicate with the Mollie API on behalf of the consenting merchant.  This endpoint can only be accessed using **OAuth client credentials**.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**authorization** | **String** | The OAuth client ID and client secret as [basic access credentials](https://en.wikipedia.org/wiki/Basic_access_authentication).  Pseudo code: `\"Basic \" + toBase64(client_id + \":\" + client_secret)`  For example: `Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==` | [required] |
**content_type** | Option<**String**> | This header value must match the type of the request body you send, if there is a request body. For example, if you send the request body as JSON, this header must be set to `application/json`, and if you send it as form encoded you must set this header to `application/x-www-form-urlencoded`. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**oauth_generate_tokens_request** | Option<[**OauthGenerateTokensRequest**](OauthGenerateTokensRequest.md)> |  |  |

### Return type

[**models::OauthGenerateTokens200Response**](oauth_generate_tokens_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## oauth_revoke_tokens

> oauth_revoke_tokens(authorization, content_type, idempotency_key, oauth_revoke_tokens_request)
Revoke tokens

Revoke an access token or refresh token. Once revoked, the token can no longer be used.  Revoking a refresh token revokes all access tokens that were created using the same authorization.  This endpoint can only be accessed using **OAuth client credentials**.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**authorization** | **String** | The OAuth client ID and client secret as [basic access credentials](https://en.wikipedia.org/wiki/Basic_access_authentication).  Pseudo code: `\"Basic \" + toBase64(client_id + \":\" + client_secret)`  For example: `Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==` | [required] |
**content_type** | Option<**String**> | This header value must match the type of the request body you send, if there is a request body. For example, if you send the request body as JSON, this header must be set to `application/json`, and if you send it as form encoded you must set this header to `application/x-www-form-urlencoded`. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**oauth_revoke_tokens_request** | Option<[**OauthRevokeTokensRequest**](OauthRevokeTokensRequest.md)> |  |  |

### Return type

 (empty response body)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

