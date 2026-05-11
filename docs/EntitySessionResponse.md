# EntitySessionResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | The resource type of the object. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this session. Mollie assigns this identifier at session creation time. Mollie will always refer to the session by this ID. Example: `sess_5B8cwPMGnU6qLbRvo7qEZo`. | [optional][readonly]
**mode** | Option<[**models::Mode**](Mode.md)> |  | [optional]
**client_access_token** | Option<**String**> | The client access token for the session. Use the client access token to initialize Mollie Components. | [optional][readonly]
**status** | Option<[**models::SessionStatus**](SessionStatus.md)> |  | [optional][readonly]
**amount** | Option<[**models::Amount**](Amount.md)> |  | [optional]
**description** | Option<**String**> | A user-friendly description of the session that may be shown to the customer during the checkout process.   Any payment created for the session will use the same description. | [optional]
**lines** | Option<[**Vec<models::SessionLineItemResponse>**](SessionLineItemResponse.md)> | List of items the customer will pay for in this session. The sum of all line items must equal the session's amount.  All lines must have the same currency as the session. | [optional]
**redirect_url** | Option<**String**> | The URL your customer will be redirected to after the payment process.  It could make sense for the redirectUrl to contain a unique identifier – like your order ID – so you can show the right page referencing the order when your customer returns. | [optional]
**billing_address** | Option<[**models::PaymentAddress**](PaymentAddress.md)> | The customer's billing address details. We advise to provide these details to improve fraud protection and conversion. | [optional]
**shipping_address** | Option<[**models::PaymentAddress**](PaymentAddress.md)> | The customer's shipping address details. We advise to provide these details to improve fraud protection and conversion. | [optional]
**customer_id** | Option<**String**> | The ID of the [customer](get-customer) the session is being created for. This is used primarily for recurring payments, but can also be used on regular payments to enable single-click payments.  If `sequenceType` is set to `first`, this field is required. | [optional]
**sequence_type** | Option<[**models::SessionSequenceTypeResponse**](SessionSequenceTypeResponse.md)> | **Only relevant for recurring payments.**  Indicate if this session is used for a one-off or a first of a recurring payment.  With a `first` payment, the customer agrees to automatic recurring charges taking place on their account in the future.  Defaults to `oneoff`, which is a regular non-recurring payment. | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Provide any data you like in a JSON object. We will save the data alongside the entity. Whenever you fetch the entity with our API, we will also include the metadata. You can use up to approximately 1kB.  Any payment created for the session will use the same metadata. | [optional]
**payment** | Option<[**models::EntitySessionPayment**](EntitySessionPayment.md)> |  | [optional]
**profile_id** | Option<**String**> | The identifier referring to the [profile](get-profile) this entity belongs to.  When using an API Key, the `profileId` must not be sent since it is linked to the key. However, for OAuth and Organization tokens, the `profileId` is required.  For more information, see [Authentication](authentication). | [optional]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**_links** | Option<[**models::EntitySessionLinks**](EntitySessionLinks.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


