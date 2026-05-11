# EntityRoute

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a route object. Will always contain the string `route` for this endpoint. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this route. Mollie assigns this identifier at route creation time. Mollie will always refer to the route by this ID. Example: `crt_dyARQ3JzCgtPDhU2Pbq3J`. | [optional][readonly]
**payment_id** | Option<**String**> | The unique identifier of the payment. For example: `tr_5B8cwPMGnU6qLbRvo7qEZo`. The full payment object can be retrieved via the payment URL in the `_links` object. | [optional][readonly]
**amount** | Option<[**models::Amount**](Amount.md)> | The amount of the route. That amount that will be routed to the specified destination. | [optional]
**description** | Option<**String**> | The description of the route. This description is shown in the reports. | [optional]
**destination** | Option<[**models::EntityRouteDestination**](EntityRouteDestination.md)> |  | [optional]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | Option<[**models::EntityRouteLinks**](EntityRouteLinks.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


