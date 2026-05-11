# GetPartnerStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **String** | Indicates the response contains a partner status object. Will always contain the string `partner` for this endpoint. | [readonly]
**partner_type** | Option<**PartnerType**> | Indicates the type of partner. Will be `null` if the currently authenticated organization is not enrolled as a partner. (enum: oauth, signuplink, useragent) | [readonly]
**is_commission_partner** | Option<**bool**> | Whether the current organization is receiving commissions. | [optional][readonly]
**user_agent_tokens** | Option<[**Vec<models::GetPartnerStatus200ResponseUserAgentTokensInner>**](GetPartnerStatus200ResponseUserAgentTokensInner.md)> | Array of User-Agent token objects. Present if the organization is a partner of type `useragent`, or if they were in the past. | [optional][readonly]
**partner_contract_signed_at** | Option<**String**> | The date the partner contract was signed, in ISO 8601 format. Omitted if no contract has been signed (yet). | [optional][readonly]
**partner_contract_update_available** | Option<**bool**> | Whether an update to the partner contract is available and requiring the organization's agreement. | [optional][readonly]
**partner_contract_expires_at** | Option<**String**> | The expiration date of the signed partner contract, in ISO 8601 format. Omitted if contract has no expiration date (yet). | [optional][readonly]
**_links** | Option<[**models::GetPartnerStatus200ResponseLinks**](GetPartnerStatus200ResponseLinks.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


