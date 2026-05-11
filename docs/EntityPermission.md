# EntityPermission

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a permission object. Will always contain the string `permission` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this permission. Example: `payments.read`. | [readonly]
**description** | **String** | A short description of what kind of access the permission enables. | [readonly]
**granted** | **bool** | Whether this permission is granted to the app by the organization. | [readonly]
**_links** | [**models::EntityBalanceLinks**](EntityBalanceLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


