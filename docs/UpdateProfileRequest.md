# UpdateProfileRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> | The profile's name, this will usually reflect the trade name or brand name of the profile's website or application. | [optional]
**website** | Option<**String**> | The URL to the profile's website or application. Only `https` or `http` URLs are allowed. No `@` signs are allowed. | [optional]
**email** | Option<**String**> | The email address associated with the profile's trade name or brand.  If the domain contains non-ASCII characters, encode it as Punycode per [RFC 3492](https://www.rfc-editor.org/rfc/rfc3492). | [optional]
**phone** | Option<**String**> | The phone number associated with the profile's trade name or brand. | [optional]
**description** | Option<**String**> | The products or services offered by the profile's website or application. | [optional]
**countries_of_activity** | Option<**Vec<String>**> | A list of countries where you expect that the majority of the profile's customers reside, in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format. | [optional]
**business_category** | Option<**String**> | The industry associated with the profile's trade name or brand. Please refer to the [business category list](common-data-types) for all possible options. | [optional]
**mode** | Option<[**models::Mode**](Mode.md)> | Updating a profile from `test` mode to `live` mode will trigger a verification process, where we review the profile before it can start accepting payments. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


