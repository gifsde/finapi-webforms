# # DirectDebitOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payer** | [**\OpenAPI\Client\Model\PaymentPayer**](PaymentPayer.md) |  |
**amount** | [**\OpenAPI\Client\Model\Amount**](Amount.md) |  |
**purpose** | **string** | The purpose of the transfer transaction | [optional]
**sepa_purpose_code** | **string** | SEPA purpose code, according to ISO 20022, external codes set.&lt;br/&gt;Please note that the SEPA purpose code may be ignored by some banks. | [optional]
**end_to_end_id** | **string** | End-To-End ID for the transfer transaction. | [optional]
**mandate_id** | **string** | Mandate ID that this direct debit order is based on. |
**mandate_date** | **\DateTime** | Date of the mandate that this direct debit order is based on, in the format &lt;code&gt;YYYY-MM-DD&lt;/code&gt; |
**creditor_id** | **string** | Creditor ID of the source account&#39;s holder |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
