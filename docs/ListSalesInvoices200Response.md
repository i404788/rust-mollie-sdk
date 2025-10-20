# ListSalesInvoices200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | Option<**i32**> | The number of items in this result set. If more items are available, a `_links.next` URL will be present in the result as well.  The maximum number of items per result set is controlled by the `limit` property provided in the request. The default limit is 50 items. | [optional]
**_embedded** | Option<[**models::ListSalesInvoices200ResponseEmbedded**](list_sales_invoices_200_response__embedded.md)> |  | [optional]
**_links** | Option<[**models::ListLinks**](list-links.md)> |  | [optional][readonly]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


