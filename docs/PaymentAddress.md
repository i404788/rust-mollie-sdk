# PaymentAddress

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> | The title of the person, for example *Mr.* or *Mrs.*. | [optional]
**given_name** | Option<**String**> | The given name (first name) of the person should be at least two characters and cannot contain only numbers.  Required for payment methods `billie`, `in3`, `klarna` and `riverty`. | [optional]
**family_name** | Option<**String**> | The given family name (surname) of the person should be at least two characters and cannot contain only numbers.  Required for payment methods `billie`, `in3`, `klarna` and `riverty`. | [optional]
**organization_name** | Option<**String**> | The name of the organization, in case the addressee is an organization. | [optional]
**street_and_number** | Option<**String**> | A street and street number.  Required for payment methods `billie`, `in3`, `klarna` and `riverty`. | [optional]
**street_additional** | Option<**String**> | Any additional addressing details, for example an apartment number. | [optional]
**postal_code** | Option<**String**> | A postal code. This field may be required if the provided country has a postal code system.  Required for payment methods `billie`, `in3`, `klarna` and `riverty`. | [optional]
**email** | Option<**String**> | A valid e-mail address.  If you provide the email address for a `banktransfer` payment, we will automatically send the instructions email upon payment creation. The language of the email will follow the locale parameter of the payment.  Required for payment methods `billie`, `in3`, `klarna` and `riverty`. | [optional]
**phone** | Option<**String**> | If provided, it must be in the [E.164](https://en.wikipedia.org/wiki/E.164) format. For example: +31208202070. | [optional]
**city** | Option<**String**> | A city name.  Required for payment methods `billie`, `in3`, `klarna` and `riverty`. | [optional]
**region** | Option<**String**> | The top-level administrative subdivision of the country. For example: Noord-Holland. | [optional]
**country** | Option<**String**> | A country code in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format.  Required for payment methods `billie`, `in3`, `klarna` and `riverty`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


