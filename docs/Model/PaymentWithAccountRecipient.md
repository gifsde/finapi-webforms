# # PaymentWithAccountRecipient

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the counterparty. Must be provided for the SEPA transfers.&lt;br/&gt;Note that neither finAPI nor the involved bank are guaranteed to validate the counterparty name. Even if the name does not depict the actual registered account holder of the target account, the order might still be successful. | [optional]
**iban** | **string** | A normalized (without spaces) IBAN of the counterparty&#39;s account |
**bic** | **string** | BIC of the counterparty&#39;s account.&lt;br/&gt;Only required for SEPA payments (i.e. payments in EUR currency), when there is no &#39;IBAN_ONLY&#39;-capability in any of the interfaces connected to the account to be used when submitting the payment. | [optional]
**address** | [**\OpenAPI\Client\Model\AddressData**](AddressData.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
