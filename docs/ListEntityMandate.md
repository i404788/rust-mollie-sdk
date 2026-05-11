# ListEntityMandate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | Option<**String**> | Indicates the response contains a mandate object. Will always contain the string `mandate` for this endpoint. | [optional][readonly]
**id** | Option<**String**> | The identifier uniquely referring to this mandate. Example: `mdt_pWUnw6pkBN`. | [optional]
**mode** | Option<[**models::Mode**](Mode.md)> |  | [optional]
**method** | Option<[**models::MandateMethodResponse**](MandateMethodResponse.md)> |  | [optional]
**consumer_name** | Option<**String**> | The customer's name. | [optional]
**consumer_account** | Option<**String**> | The customer's IBAN. Required for SEPA Direct Debit mandates. | [optional]
**consumer_bic** | Option<**String**> | The BIC of the customer's bank. | [optional]
**consumer_email** | Option<**String**> | The customer's email address. Required for PayPal mandates. | [optional]
**details** | Option<[**models::ListEntityMandateDetails**](ListEntityMandateDetails.md)> |  | [optional]
**signature_date** | Option<**String**> | The date when the mandate was signed in `YYYY-MM-DD` format. | [optional]
**mandate_reference** | Option<**String**> | A custom mandate reference. For SEPA Direct Debit, it is vital to provide a unique reference. Some banks will decline Direct Debit payments if the mandate reference is not unique. | [optional]
**paypal_billing_agreement_id** | Option<**String**> | The billing agreement ID given by PayPal. For example: `B-12A34567B8901234CD`. Required for PayPal mandates. Must provide either this field or `payPalVaultId`, but not both. | [optional]
**pay_pal_vault_id** | Option<**String**> | The Vault ID given by PayPal. For example: `8kk8451t`. Required for PayPal mandates. Must provide either this field or `paypalBillingAgreementId`, but not both. | [optional]
**scopes** | Option<[**Vec<models::MandateScopesResponse>**](MandateScopesResponse.md)> | An array defining the eligible use cases for the mandate. This field will always be  present and can contain one or both of the following values: | [optional][readonly]
**status** | Option<[**models::MandateStatusResponse**](MandateStatusResponse.md)> |  | [optional][readonly]
**customer_id** | Option<**String**> | The identifier referring to the [customer](get-customer) this mandate was linked to. | [optional][readonly]
**created_at** | Option<**String**> | The entity's date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. | [optional][readonly]
**testmode** | Option<**bool**> | Whether to create the entity in test mode or live mode.  Most API credentials are specifically created for either live mode or test mode, in which case this parameter must not be sent. For organization-level credentials such as OAuth access tokens, you can enable test mode by setting `testmode` to `true`. | [optional]
**_links** | Option<[**models::ListEntityMandateLinks**](ListEntityMandateLinks.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


