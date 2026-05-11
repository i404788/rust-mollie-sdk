# EntityPaymentRoute

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a route object. Will always contain the string `route` for this endpoint. | [readonly]
**id** | **String** | The identifier uniquely referring to this route. Mollie will always refer to the route by this ID. Example: `rt_5B8cwPMGnU6qLbRvo7qEZo`. | [readonly]
**mode** | [**models::Mode**](Mode.md) |  | 
**amount** | [**models::Amount**](Amount.md) | The portion of the total payment amount being routed. Currently only `EUR` payments can be routed. | 
**destination** | [**models::EntityPaymentRouteDestination**](EntityPaymentRouteDestination.md) |  | 
**created_at** | **String** | The date and time when the route was created. The date is given in ISO 8601 format. | [readonly]
**release_date** | Option<**String**> | Optionally, schedule this portion of the payment to be transferred to its destination on a later date. The date must be given in `YYYY-MM-DD` format.  If no date is given, the funds become available to the connected merchant as soon as the payment succeeds. | [optional]
**_links** | [**models::EntityPaymentRouteLinks**](EntityPaymentRouteLinks.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


