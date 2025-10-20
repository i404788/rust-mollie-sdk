# SubmitOnboardingDataRequestOrganization

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> | The name of the organization. | [optional]
**address** | Option<[**models::Address**](address.md)> | The address of the organization. | [optional]
**registration_number** | Option<**String**> | The registration number of the organization at their local chamber of commerce. | [optional]
**vat_number** | Option<**String**> | The VAT number of the organization, if based in the European Union or in The United Kingdom. VAT numbers are verified against the international registry *VIES*.  The field can be omitted for merchants residing in other countries. | [optional]
**vat_regulation** | Option<**String**> | Mollie applies Dutch VAT for merchants based in The Netherlands, British VAT for merchants based in The United Kingdom, and shifted VAT for merchants in the European Union.  The field can be omitted for merchants residing in other countries. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


