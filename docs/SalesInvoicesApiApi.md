# \SalesInvoicesApiApi

All URIs are relative to *https://api.mollie.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_sales_invoice**](SalesInvoicesApiApi.md#create_sales_invoice) | **POST** /sales-invoices | Create sales invoice
[**delete_sales_invoice**](SalesInvoicesApiApi.md#delete_sales_invoice) | **DELETE** /sales-invoices/{id} | Delete sales invoice
[**get_sales_invoice**](SalesInvoicesApiApi.md#get_sales_invoice) | **GET** /sales-invoices/{id} | Get sales invoice
[**list_sales_invoices**](SalesInvoicesApiApi.md#list_sales_invoices) | **GET** /sales-invoices | List sales invoices
[**update_sales_invoice**](SalesInvoicesApiApi.md#update_sales_invoice) | **PATCH** /sales-invoices/{id} | Update sales invoice



## create_sales_invoice

> models::EntitySalesInvoiceResponse create_sales_invoice(idempotency_key, entity_sales_invoice)
Create sales invoice

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  With the Sales Invoice API you can generate sales invoices to send to your customers.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**entity_sales_invoice** | Option<[**EntitySalesInvoice**](EntitySalesInvoice.md)> |  |  |

### Return type

[**models::EntitySalesInvoiceResponse**](entity-sales-invoice-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_sales_invoice

> serde_json::Value delete_sales_invoice(id, idempotency_key, delete_values_sales_invoice)
Delete sales invoice

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Sales invoices which are in status `draft` can be deleted. For all other statuses, please use the [Update sales invoice](update-sales-invoice) endpoint instead.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**delete_values_sales_invoice** | Option<[**DeleteValuesSalesInvoice**](DeleteValuesSalesInvoice.md)> |  |  |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_sales_invoice

> models::EntitySalesInvoiceResponse get_sales_invoice(id, testmode, idempotency_key)
Get sales invoice

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Retrieve a single sales invoice by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::EntitySalesInvoiceResponse**](entity-sales-invoice-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sales_invoices

> models::ListSalesInvoices200Response list_sales_invoices(from, limit, testmode, idempotency_key)
List sales invoices

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Retrieve a list of all sales invoices created through the API.  The results are paginated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from** | Option<**String**> | Provide an ID to start the result set from the item with the given ID and onwards. This allows you to paginate the result set. |  |
**limit** | Option<**i32**> | The maximum number of items to return. Defaults to 50 items. |  |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSalesInvoices200Response**](list_sales_invoices_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_sales_invoice

> models::EntitySalesInvoiceResponse update_sales_invoice(id, idempotency_key, update_values_sales_invoice)
Update sales invoice

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Certain details of an existing sales invoice can be updated. For `draft` it is all values listed below, but for statuses `paid` and `issued` there are certain additional requirements (`paymentDetails` and `emailDetails`, respectively).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Provide the ID of the item you want to perform this operation on. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**update_values_sales_invoice** | Option<[**UpdateValuesSalesInvoice**](UpdateValuesSalesInvoice.md)> |  |  |

### Return type

[**models::EntitySalesInvoiceResponse**](entity-sales-invoice-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

