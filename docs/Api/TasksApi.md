# OpenAPI\Client\TasksApi

All URIs are relative to https://webform-sandbox.finapi.io, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getTask()**](TasksApi.md#getTask) | **GET** /api/tasks/{id} | Get a task |
| [**getTasks()**](TasksApi.md#getTasks) | **GET** /api/tasks | Get tasks |


## `getTask()`

```php
getTask($id): \OpenAPI\Client\Model\Task
```

Get a task

Get a task of the authorized user.<br/><br/>Must pass the user's access token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identifier of the task

try {
    $result = $apiInstance->getTask($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->getTask: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Identifier of the task | |

### Return type

[**\OpenAPI\Client\Model\Task**](../Model/Task.md)

### Authorization

[BearerAccessToken](../../README.md#BearerAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTasks()`

```php
getTasks($order, $page, $per_page): \OpenAPI\Client\Model\TasksPage
```

Get tasks

Get all tasks associated with the authorized user.<br/><br/>Must pass the user's access token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TasksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order = createdAt,desc; // string | Determines the order of the results. You can order by <code>createdAt</code> field ascending or descending. The general format is <code>property[,asc|desc]</code>, with <code>asc</code> being the default value.The default order is <code>createdAt,asc</code>.
$page = 1; // int | Page to load
$per_page = 20; // int | The number of items on the page

try {
    $result = $apiInstance->getTasks($order, $page, $per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TasksApi->getTasks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order** | **string**| Determines the order of the results. You can order by &lt;code&gt;createdAt&lt;/code&gt; field ascending or descending. The general format is &lt;code&gt;property[,asc|desc]&lt;/code&gt;, with &lt;code&gt;asc&lt;/code&gt; being the default value.The default order is &lt;code&gt;createdAt,asc&lt;/code&gt;. | [optional] |
| **page** | **int**| Page to load | [optional] [default to 1] |
| **per_page** | **int**| The number of items on the page | [optional] [default to 20] |

### Return type

[**\OpenAPI\Client\Model\TasksPage**](../Model/TasksPage.md)

### Authorization

[BearerAccessToken](../../README.md#BearerAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
