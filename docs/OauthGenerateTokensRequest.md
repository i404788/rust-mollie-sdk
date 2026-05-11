# OauthGenerateTokensRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**grant_type** | [**models::OauthGrantType**](OauthGrantType.md) | If you wish to exchange your authorization code for an app access token, use grant type `authorization_code`. If you wish to renew your app access token with your refresh token, use grant type `refresh_token`. | 
**code** | Option<**String**> | The authorization code you received when creating the authorization. Only use this field when using grant type `authorization_code`. | [optional]
**refresh_token** | Option<**String**> | The refresh token you received when creating the authorization. Only use this field when using grant type `refresh_token`. | [optional]
**redirect_uri** | Option<**String**> | The URL the merchant is sent back to once the request has been authorized. It must match the URL you set when registering your app.  For consecutive refresh token requests, this parameter is required only if the initial authorization code grant request also contained a `redirect_uri`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


