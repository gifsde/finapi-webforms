# # TaskCallbacks

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**finalised** | **string** | URL to which finAPI sends the notification message after the task is finalised (either completed successfully or with an error).&lt;br/&gt;finAPI will call this URL with HTTP method POST ignoring the response of the target endpoint. Only HTTPS URLs are allowed. | [optional]
**web_form_required** | **string** | URL to which finAPI sends the notification message when the update can longer run in the background.&lt;br/&gt;finAPI will call this URL with HTTP method POST ignoring the response of the target endpoint. Only HTTPS URLs are allowed. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
