# # Language

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**selector** | **string** | Whether the language selector in the web form header will be displayed.&lt;br/&gt;&lt;strong&gt;NOTE:&lt;/strong&gt; in case &lt;code&gt;functionality.header&lt;/code&gt; is marked as &lt;code&gt;HIDDEN&lt;/code&gt;, then this property will be ignored.&lt;br/&gt;&lt;strong&gt;NOTE:&lt;/strong&gt; If no value is provided, then the following value will be applied by default when web form is opened: &lt;code&gt;RENDER&lt;/code&gt;. | [optional]
**locked** | **string** | The language in which the web form will be shown. The language must be given in the &lt;a target&#x3D;&#39;_blank&#39; href&#x3D;&#39;https://www.iso.org/iso-639-language-codes.html&#39;&gt;ISO-639&lt;/a&gt; 2 letter code format.&lt;br/&gt;&amp;bull; This must be initialized if either the &lt;code&gt;functionality.header&lt;/code&gt; or &lt;code&gt;functionality.language.selector&lt;/code&gt; are &lt;code&gt;HIDDEN&lt;/code&gt;;&lt;br/&gt;&amp;bull; This must be null if both &lt;code&gt;functionality.header&lt;/code&gt; and &lt;code&gt;functionality.language.selector&lt;/code&gt; are set to &lt;code&gt;RENDER&lt;/code&gt;.&lt;br/&gt;&lt;strong&gt;NOTE:&lt;/strong&gt; If no value is provided, then the following value will be applied by default when web form is opened: &lt;code&gt;null&lt;/code&gt;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
