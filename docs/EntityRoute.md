# EntityRoute

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a route object. Will always contain the string `route` for this endpoint. | [optional][readonly]
**id** | Option<**String**> |  | [optional]
**payment_id** | Option<**String**> |  | [optional]
**amount** | Option<[**models::Amount**](amount.md)> | The amount of the route. That amount that will be routed to the specified destination. | [optional]
**description** | Option<**String**> | The description of the route. This description is shown in the reports. | [optional]
**destination** | Option<[**models::EntityRouteDestination**](entity_route_destination.md)> |  | [optional]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**_links** | Option<[**models::EntityWebhookLinks**](entity_webhook__links.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


