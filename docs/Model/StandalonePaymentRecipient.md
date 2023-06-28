# # StandalonePaymentRecipient

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the counterparty.&lt;br/&gt;Note that neither finAPI nor the involved bank are guaranteed to validate the counterparty name. Even if the name does not depict the actual registered account holder of the target account, the order might still be successful. |
**iban** | **string** | A normalized (without spaces) IBAN of the counterparty&#39;s account |
**bic** | **string** | BIC of the counterparty&#39;s account | [optional]
**address** | [**\OpenAPI\Client\Model\AddressData**](AddressData.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
