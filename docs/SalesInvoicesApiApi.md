# \SalesInvoicesApiApi

All URIs are relative to *https://api.mollie.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_sales_invoice**](SalesInvoicesApiApi.md#create_sales_invoice) | **POST** /v2/sales-invoices | Create sales invoice
[**delete_sales_invoice**](SalesInvoicesApiApi.md#delete_sales_invoice) | **DELETE** /v2/sales-invoices/{salesInvoiceId} | Delete sales invoice
[**get_sales_invoice**](SalesInvoicesApiApi.md#get_sales_invoice) | **GET** /v2/sales-invoices/{salesInvoiceId} | Get sales invoice
[**list_sales_invoices**](SalesInvoicesApiApi.md#list_sales_invoices) | **GET** /v2/sales-invoices | List sales invoices
[**update_sales_invoice**](SalesInvoicesApiApi.md#update_sales_invoice) | **PATCH** /v2/sales-invoices/{salesInvoiceId} | Update sales invoice



## create_sales_invoice

> models::SalesInvoiceResponse create_sales_invoice(idempotency_key, sales_invoice_request)
Create sales invoice

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  With the Sales Invoice API you can generate sales invoices to send to your customers.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**sales_invoice_request** | Option<[**SalesInvoiceRequest**](SalesInvoiceRequest.md)> |  |  |

### Return type

[**models::SalesInvoiceResponse**](sales-invoice-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_sales_invoice

> delete_sales_invoice(sales_invoice_id, idempotency_key, delete_values_sales_invoice)
Delete sales invoice

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Sales invoices which are in status `draft` can be deleted. For all other statuses, please use the [Update sales invoice](update-sales-invoice) endpoint instead.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sales_invoice_id** | **String** | Provide the ID of the related sales invoice. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**delete_values_sales_invoice** | Option<[**DeleteValuesSalesInvoice**](DeleteValuesSalesInvoice.md)> |  |  |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_sales_invoice

> models::SalesInvoiceResponse get_sales_invoice(sales_invoice_id, testmode, idempotency_key)
Get sales invoice

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Retrieve a single sales invoice by its ID.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sales_invoice_id** | **String** | Provide the ID of the related sales invoice. | [required] |
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::SalesInvoiceResponse**](sales-invoice-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

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
**testmode** | Option<**bool**> | Most API credentials are specifically created for either live mode or test mode. In those cases the `testmode` query parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting the `testmode` query parameter to `true`.  Test entities cannot be retrieved when the endpoint is set to live mode, and vice versa. |  |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |

### Return type

[**models::ListSalesInvoices200Response**](list_sales_invoices_200_response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_sales_invoice

> models::SalesInvoiceResponse update_sales_invoice(sales_invoice_id, idempotency_key, update_sales_invoice_request)
Update sales invoice

> 🚧 Beta feature > > This feature is currently in beta testing, and the final specification may still change.  Certain details of an existing sales invoice can be updated. For `draft` it is all values listed below, but for statuses `paid` and `issued` there are certain additional requirements (`paymentDetails` and `emailDetails`, respectively).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sales_invoice_id** | **String** | Provide the ID of the related sales invoice. | [required] |
**idempotency_key** | Option<**String**> | A unique key to ensure idempotent requests. This key should be a UUID v4 string. |  |
**update_sales_invoice_request** | Option<[**UpdateSalesInvoiceRequest**](UpdateSalesInvoiceRequest.md)> |  |  |

### Return type

[**models::SalesInvoiceResponse**](sales-invoice-response.md)

### Authorization

[apiKey](../README.md#apiKey), [oAuth](../README.md#oAuth), [organizationAccessToken](../README.md#organizationAccessToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/hal+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

