# \InvoicesApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_invoice**](InvoicesApiApi.md#get_invoice) | **GET** /invoices/{id} | Get invoice
[**list_invoices**](InvoicesApiApi.md#list_invoices) | **GET** /invoices | List invoices



## get_invoice

> models::EntityInvoice get_invoice(id, idempotency_key)
Get invoice

Retrieve a single invoice by its ID.  If you want to retrieve the details of an invoice by its invoice number, call the [List invoices](list-invoices) endpoint with the `reference` parameter.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntityInvoice**](entity-invoice.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_invoices

> models::ListInvoices200Response list_invoices(reference, year, month, from, limit, sort, idempotency_key)
List invoices

Retrieve a list of all your invoices, optionally filtered by year or by invoice reference.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**reference** | Option<**String**> | Filter for an invoice with a specific invoice reference, for example `2024.10000`. |  |
**year** | Option<**String**> | Filter for invoices of a specific year, for example `2024`. |  |
**month** | Option<**String**> | Filter for invoices of a specific month, for example `01`. |  |
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**sort** | Option<**String**> | Used for setting the direction of the result set. Defaults to descending order, meaning the results are ordered from newest to oldest. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListInvoices200Response**](list_invoices_200_response.md)

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

