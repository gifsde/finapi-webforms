# # StandalonePaymentOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**recipient** | [**\OpenAPI\Client\Model\StandalonePaymentRecipient**](StandalonePaymentRecipient.md) |  |
**amount** | [**\OpenAPI\Client\Model\Amount**](Amount.md) |  |
**purpose** | **string** | The purpose of the transfer transaction | [optional]
**sepa_purpose_code** | **string** | SEPA purpose code, according to ISO 20022, external codes set.&lt;br/&gt;Please note that the SEPA purpose code may be ignored by some banks. | [optional]
**end_to_end_id** | **string** | End-To-End ID for the transfer transaction. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
