# ErrorResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **i32** | The status code of the error message. This is always the same code as the status code of the HTTP message itself. | 
**title** | **String** | The HTTP reason phrase of the error. For example, for a `404` error, the `title` will be `Not Found`. | 
**detail** | **String** | A detailed human-readable description of the error that occurred. | 
**field** | Option<**String**> | If the error was caused by a value provided by you in a specific field, the `field` property will contain the name of the field that caused the issue. | [optional]
**_links** | [**models::ErrorResponseLinks**](error_response__links.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


