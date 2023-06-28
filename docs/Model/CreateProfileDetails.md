# # CreateProfileDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **string** | Label to profile.&lt;br/&gt;The label must be unique. |
**default** | **bool** | Whether the profile will be used by default for all web forms. Default value is &lt;code&gt;false&lt;/code&gt;.&lt;br/&gt;We urge you to set one profile as default. This way, if you do not pass the profile in the API call, we will use the default profile from you for the web forms.&lt;br/&gt;&lt;br/&gt;There can only be one default profile at one time. | [optional] [default to false]
**brand** | [**\OpenAPI\Client\Model\Brand**](Brand.md) |  | [optional]
**functionality** | [**\OpenAPI\Client\Model\Functionality**](Functionality.md) |  | [optional]
**aspect** | [**\OpenAPI\Client\Model\Aspect**](Aspect.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
