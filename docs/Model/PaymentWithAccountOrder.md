# # PaymentWithAccountOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**recipient** | [**\OpenAPI\Client\Model\PaymentWithAccountRecipient**](PaymentWithAccountRecipient.md) |  |
**structured_remittance_information** | **string[]** | This attribute is used to submit structured remittance information for the domestic payments. Please refer to the documentation for more details. For more information, please check the &lt;a href&#x3D;\&quot;https://documentation.finapi.io/payments/Czech-Republic-Domestic-Transfers.3045916711.html\&quot;&gt;FAQ article&lt;/a&gt;. | [optional]
**amount** | [**\OpenAPI\Client\Model\Amount**](Amount.md) |  |
**purpose** | **string** | The purpose of the transfer transaction | [optional]
**sepa_purpose_code** | **string** | SEPA purpose code, according to ISO 20022, external codes set.&lt;br/&gt;Please note that the SEPA purpose code may be ignored by some banks. Only applicable for the SEPA transfers and will be discarded for other transfers. | [optional]
**end_to_end_id** | **string** | End-To-End ID for the transfer transaction. Only applicable for the SEPA transfers and will be discarded for other transfers. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
