# OauthGenerateTokens200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_token** | Option<**String**> | The app access token, with which you will be able to access the Mollie API on the merchant's behalf. | [optional]
**refresh_token** | Option<**String**> | The refresh token, with which you will be able to retrieve new app access tokens on this endpoint. The refresh token does not expire. | [optional]
**expires_in** | Option<**i32**> | The number of seconds left before the app access token expires. Be sure to renew your app access token before this reaches zero. | [optional]
**token_type** | Option<**String**> | As per OAuth standards, the provided app access token can only be used with `bearer` authentication.  Possible values: `bearer` | [optional]
**scope** | Option<**String**> | A space-separated list of [permissions](https://docs.mollie.com/docs/permissions). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


