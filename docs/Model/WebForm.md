# # WebForm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Globally unique web form&#39;s identifier |
**url** | **string** | Full web form&#39;s URL (including the hostname).&lt;br/&gt;You can enhance the given URL with the following query parameters: &lt;code&gt;redirectUrl&lt;/code&gt;, &lt;code&gt;errorRedirectUrl&lt;/code&gt;, &lt;code&gt;abortRedirectUrl&lt;/code&gt;, &lt;code&gt;customerSupportUrl&lt;/code&gt;.&lt;br/&gt;Find more info in the &lt;a href&#x3D;&#39;https://documentation.finapi.io/webform/For-best-results!.2477654019.html#Forbestresults!-Enhanceend-userexperience!&#39; target&#x3D;&#39;_blank&#39;&gt;Web Form 2.0 Public Documentation&lt;/a&gt;. |
**created_at** | **\DateTime** | The timestamp when the web form was created in the format &lt;code&gt;yyyy-MM-dd&#39;T&#39;HH:mm:ss.SSSZ&lt;/code&gt;. |
**expires_at** | **\DateTime** | The timestamp when the web form expires in the format &lt;code&gt;yyyy-MM-dd&#39;T&#39;HH:mm:ss.SSSZ&lt;/code&gt;. |
**type** | [**\OpenAPI\Client\Model\WebFormType**](WebFormType.md) |  |
**status** | [**\OpenAPI\Client\Model\WebFormStatus**](WebFormStatus.md) |  |
**payload** | [**\OpenAPI\Client\Model\Payload**](Payload.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
