# # TaskPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bank_connection_id** | **int** | Identifier of the bank connection in the Access API. Initialized as soon as the task process is started. Use those ID to gather Bank Connection data from Access endpoints like, \&quot;&lt;a target&#x3D;&#39;_blank&#39; href&#x3D;&#39;https://docs.finapi.io/?product&#x3D;access#get-/api/v1/bankConnections/-id-&#39;&gt;Get a bank connection&lt;/a&gt;\&quot; or \&quot;&lt;a target&#x3D;&#39;_blank&#39; href&#x3D;&#39;https://docs.finapi.io/?product&#x3D;access#get-/api/v1/accounts&#39;&gt;Get and search all accounts&lt;/a&gt;\&quot;. |
**web_form** | [**\OpenAPI\Client\Model\WebFormInfo**](WebFormInfo.md) |  | [optional]
**error_code** | **string** | Reason of the task failure.&lt;br/&gt;&lt;strong&gt;NOTE:&lt;/strong&gt; This enum can be extended in the future as new cases arise!&lt;br/&gt;&lt;br/&gt;Codes can be interpreted as follows:&lt;br/&gt;&amp;bull; &lt;code&gt;BANK_SERVER_REJECTION&lt;/code&gt; - the flow has been terminated on the bank side, e.g., in case of incorrect credentials;&lt;br/&gt;&amp;bull; &lt;code&gt;INVALID_TOKEN&lt;/code&gt; - the given access token expired or became invalid during the flow; &lt;br/&gt;&amp;bull; &lt;code&gt;UNEXPECTED_ACCESS_RESPONSE&lt;/code&gt; - an unexpected response has been received from the Access API - similarly to the &lt;code&gt;INTERNAL_ERROR&lt;/code&gt; code, please forward all details to our Customer Support team; &lt;br/&gt;&amp;bull; &lt;code&gt;INTERNAL_ERROR&lt;/code&gt; - the reason of the failure can not be identified - please forward all the details to our Customer Support team in order to get more info and also help us to eliminate the issue. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
