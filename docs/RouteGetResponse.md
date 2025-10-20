# RouteGetResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a route object. Will always contain the string `route` for this endpoint. | [readonly]
**id** | **String** |  | 
**payment_id** | **String** |  | 
**amount** | [**models::Amount**](amount.md) | The amount of the route. That amount that will be routed to the specified destination. | 
**description** | **String** | The description of the route. This description is shown in the reports. | 
**destination** | [**models::EntityRouteDestination**](entity_route_destination.md) |  | 
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter can be omitted. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**_links** | [**models::EntityWebhookLinks**](entity_webhook__links.md) |  | 
**created_at** | **String** | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [readonly]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


