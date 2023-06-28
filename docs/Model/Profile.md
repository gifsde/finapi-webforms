# # Profile

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Globally unique profile&#39;s identifier |
**label** | **string** | Label to profile |
**created_at** | **\DateTime** | The timestamp when the profile was created in the format &lt;code&gt;yyyy-MM-dd&#39;T&#39;HH:mm:ss.SSSZ&lt;/code&gt;. |
**default** | **bool** | Whether the profile will be used by default for all web forms.&lt;br/&gt;We urge you to set one profile as default. This way, if you do not pass the profile in the API call, we will use the default profile from you for the web forms. |
**brand** | [**\OpenAPI\Client\Model\Brand**](Brand.md) |  | [optional]
**functionality** | [**\OpenAPI\Client\Model\Functionality**](Functionality.md) |  | [optional]
**aspect** | [**\OpenAPI\Client\Model\Aspect**](Aspect.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
