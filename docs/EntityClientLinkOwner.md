# EntityClientLinkOwner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **String** | The email address of your customer.  If the domain contains non-ASCII characters, encode it as Punycode per [RFC 3492](https://www.rfc-editor.org/rfc/rfc3492). | 
**given_name** | **String** | The given name (first name) of your customer. | 
**family_name** | **String** | The family name (surname) of your customer. | 
**locale** | Option<[**models::LocaleResponse**](LocaleResponse.md)> | Preset the language to be used for the login screen, if applicable. For the consent screen, the preferred language of the logged in merchant will be used and this parameter is ignored.  When this parameter is omitted, the browser language will be used instead. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


