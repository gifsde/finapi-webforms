# # StandingOrderDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | [**\OpenAPI\Client\Model\Amount**](Amount.md) |  |
**purpose** | **string** | The purpose of the transfer transaction | [optional]
**sepa_purpose_code** | **string** | SEPA purpose code, according to ISO 20022, external codes set.&lt;br/&gt;Please note that the SEPA purpose code may be ignored by some banks. | [optional]
**end_to_end_id** | **string** | End-To-End ID for the transfer transaction. | [optional]
**recipient** | [**\OpenAPI\Client\Model\Recipient**](Recipient.md) |  |
**sender** | [**\OpenAPI\Client\Model\Sender**](Sender.md) |  | [optional]
**start_date** | **\DateTime** | Date when the 1st of the standing orders should be executed, in the format &lt;code&gt;YYYY-MM-DD&lt;/code&gt;. The date may not be in the past. |
**end_date** | **\DateTime** | Date by when the last standing order in the request should be executed, in the format &lt;code&gt;YYYY-MM-DD&lt;/code&gt;. If is not provided, it is an infinite standing order. This date must be after the start date. | [optional]
**frequency** | **string** | The frequency of the recurring payment resulting from the standing order. |
**profile_id** | **string** | The profile to be applied to the web form.&lt;br/&gt;This will overwrite the default profile, if such a profile exists. | [optional]
**redirect_url** | **string** | The URL where the end-user will be redirected to after completing the bank login and (possibly) the SCA on the bank&#39;s website. Must always be provided by mandators with &lt;code&gt;FULLY_LICENSED&lt;/code&gt; or &lt;code&gt;PISP&lt;/code&gt; license type, and may not be provided by mandators with other license types. Find more info in the &lt;a target&#x3D;&#39;_blank&#39; href&#x3D;&#39;https://documentation.finapi.io/webform/Licensed-customers-using-the-Web-Form.2832302195.html&#39;&gt;Web Form 2.0 Public Documentation&lt;/a&gt;.&lt;br/&gt;&lt;br/&gt;&lt;strong&gt;NOTE:&lt;/strong&gt; Please note that this URL is used during the bank authentication flow. If you would like to provide a URL to which the end user will get redirected at the &lt;strong&gt;end of the web form flow&lt;/strong&gt;, please check out the &lt;a href&#x3D;&#39;https://documentation.finapi.io/webform/For-best-results!.2477654019.html#Forbestresults!-Enhanceend-userexperience!&#39; target&#x3D;&#39;_blank&#39;&gt;Web Form 2.0 Public Documentation&lt;/a&gt;. | [optional]
**callbacks** | [**\OpenAPI\Client\Model\Callbacks**](Callbacks.md) |  | [optional]
**allow_test_bank** | **bool** | Whether the bank search will include the test banks in the search results. When set to false, all test banks will be excluded from the bank search results. | [optional] [default to true]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
