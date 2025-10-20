# \ClientsApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_client**](ClientsApiApi.md#get_client) | **GET** /clients/{id} | Get client
[**list_clients**](ClientsApiApi.md#list_clients) | **GET** /clients | List clients



## get_client

> models::ListClients200ResponseEmbeddedClientsInner get_client(id, embed, idempotency_key)
Get client

Retrieve a single client by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListClients200ResponseEmbeddedClientsInner**](list_clients_200_response__embedded_clients_inner.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_clients

> models::ListClients200Response list_clients(embed, from, limit, idempotency_key)
List clients

Retrieve a list of all clients linked to your account.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**embed** | Option<**String**> | This endpoint allows embedding related API items by appending the following values via the `embed` query string parameter. |  |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListClients200Response**](list_clients_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

