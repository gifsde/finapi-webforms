# OpenAPI\Client\WebFormsApi

All URIs are relative to https://webform-sandbox.finapi.io, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteWebForm()**](WebFormsApi.md#deleteWebForm) | **DELETE** /api/webForms/{id} | Delete a web form |
| [**getWebForm()**](WebFormsApi.md#getWebForm) | **GET** /api/webForms/{id} | Get a web form |
| [**getWebForms()**](WebFormsApi.md#getWebForms) | **GET** /api/webForms | Get web forms |


## `deleteWebForm()`

```php
deleteWebForm($id)
```

Delete a web form

Delete a web form of the user that is authorized by the access token.<br/><br/>Must pass the user's access token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WebFormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identifier of the web form

try {
    $apiInstance->deleteWebForm($id);
} catch (Exception $e) {
    echo 'Exception when calling WebFormsApi->deleteWebForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Identifier of the web form | |

### Return type

void (empty response body)

### Authorization

[BearerAccessToken](../../README.md#BearerAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWebForm()`

```php
getWebForm($id): \OpenAPI\Client\Model\WebForm
```

Get a web form

Get a web form of the authorized user.<br/><br/>Must pass the user's access token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WebFormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identifier of the web form

try {
    $result = $apiInstance->getWebForm($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebFormsApi->getWebForm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Identifier of the web form | |

### Return type

[**\OpenAPI\Client\Model\WebForm**](../Model/WebForm.md)

### Authorization

[BearerAccessToken](../../README.md#BearerAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWebForms()`

```php
getWebForms($order, $page, $per_page): \OpenAPI\Client\Model\WebFormsPage
```

Get web forms

Get all web forms associated with the authorized user.<br/><br/>Must pass the user's access token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WebFormsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order = createdAt,desc; // string | Determines the order of the results. You can order by <code>createdAt</code> field ascending or descending. The general format is <code>property[,asc|desc]</code>, with <code>asc</code> being the default value.The default order is <code>createdAt,asc</code>.
$page = 1; // int | Page to load
$per_page = 20; // int | The number of items on the page

try {
    $result = $apiInstance->getWebForms($order, $page, $per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebFormsApi->getWebForms: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order** | **string**| Determines the order of the results. You can order by &lt;code&gt;createdAt&lt;/code&gt; field ascending or descending. The general format is &lt;code&gt;property[,asc|desc]&lt;/code&gt;, with &lt;code&gt;asc&lt;/code&gt; being the default value.The default order is &lt;code&gt;createdAt,asc&lt;/code&gt;. | [optional] |
| **page** | **int**| Page to load | [optional] [default to 1] |
| **per_page** | **int**| The number of items on the page | [optional] [default to 20] |

### Return type

[**\OpenAPI\Client\Model\WebFormsPage**](../Model/WebFormsPage.md)

### Authorization

[BearerAccessToken](../../README.md#BearerAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
