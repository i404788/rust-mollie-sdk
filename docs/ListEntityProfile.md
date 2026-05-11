# ListEntityProfile

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a profile object. Will always contain the string `profile` for this endpoint. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this profile. Example: `pfl_v9hTwCvYqw`. | [optional][readonly]
**mode** | Option<[**models::Mode**](Mode.md)> |  | [optional]
**name** | Option<**String**> | The profile's name, this will usually reflect the trade name or brand name of the profile's website or application. | [optional]
**website** | Option<**String**> | The URL to the profile's website or application. Only `https` or `http` URLs are allowed. No `@` signs are allowed. | [optional]
**email** | Option<**String**> | The email address associated with the profile's trade name or brand.  If the domain contains non-ASCII characters, encode it as Punycode per [RFC 3492](https://www.rfc-editor.org/rfc/rfc3492). | [optional]
**phone** | Option<**String**> | The phone number associated with the profile's trade name or brand. | [optional]
**description** | Option<**String**> | The products or services offered by the profile's website or application. | [optional]
**countries_of_activity** | Option<**Vec<String>**> | A list of countries where you expect that the majority of the profile's customers reside, in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format. | [optional]
**business_category** | Option<**String**> | The industry associated with the profile's trade name or brand. Please refer to the [business category list](common-data-types#business-category) for all possible options. | [optional]
**status** | Option<[**models::ProfileStatusResponse**](ProfileStatusResponse.md)> |  | [optional][readonly]
**review** | Option<[**models::ListEntityProfileReview**](ListEntityProfileReview.md)> |  | [optional]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | Option<[**models::ListEntityProfileLinks**](ListEntityProfileLinks.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


