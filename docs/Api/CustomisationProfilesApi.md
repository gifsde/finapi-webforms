# OpenAPI\Client\CustomisationProfilesApi

All URIs are relative to https://webform-sandbox.finapi.io, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createProfile()**](CustomisationProfilesApi.md#createProfile) | **POST** /api/profiles | Create a profile |
| [**deleteProfile()**](CustomisationProfilesApi.md#deleteProfile) | **DELETE** /api/profiles/{id} | Delete a profile |
| [**editProfile()**](CustomisationProfilesApi.md#editProfile) | **PATCH** /api/profiles/{id} | Edit a profile |
| [**getProfile()**](CustomisationProfilesApi.md#getProfile) | **GET** /api/profiles/{id} | Get a profile |
| [**getProfiles()**](CustomisationProfilesApi.md#getProfiles) | **GET** /api/profiles | Get profiles |


## `createProfile()`

```php
createProfile($create_profile_details): \OpenAPI\Client\Model\Profile
```

Create a profile

The endpoint provides a list of parameters which customers can personalize to be in line with their brand's styling.<br/>The endpoint triggered with a list of values, will create a profile with a unique <code>profileId</code>. When the customer passes the <code>profileId</code> on an API call, the values from the profile are applied on the web form while rendering to end-users. We welcome customers to set up a default profile, so that they do not need to pass the <code>profileId</code> as a parameter for every API call.<br/><br/>In case the API request is syntactically correct, the service will respond with HTTP return code 201 and a profile object.<br/><br/>Must pass the <a href='https://documentation.finapi.io/access/Application-management.2763423767.html' target='_blank'>mandator admin client</a>'s access_token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomisationProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_profile_details = new \OpenAPI\Client\Model\CreateProfileDetails(); // \OpenAPI\Client\Model\CreateProfileDetails

try {
    $result = $apiInstance->createProfile($create_profile_details);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomisationProfilesApi->createProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_profile_details** | [**\OpenAPI\Client\Model\CreateProfileDetails**](../Model/CreateProfileDetails.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Profile**](../Model/Profile.md)

### Authorization

[BearerAccessToken](../../README.md#BearerAccessToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteProfile()`

```php
deleteProfile($id)
```

Delete a profile

Delete a single profile by its id.<br/><br/>Must pass the <a href='https://documentation.finapi.io/access/Application-management.2763423767.html' target='_blank'>mandator admin client</a>'s access_token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomisationProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identifier of the profile

try {
    $apiInstance->deleteProfile($id);
} catch (Exception $e) {
    echo 'Exception when calling CustomisationProfilesApi->deleteProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Identifier of the profile | |

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

## `editProfile()`

```php
editProfile($id, $edit_profile_details): \OpenAPI\Client\Model\Profile
```

Edit a profile

Edit a single profile by its id.<br/><br/>Must pass the <a href='https://documentation.finapi.io/access/Application-management.2763423767.html' target='_blank'>mandator admin client</a>'s access_token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomisationProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identifier of the profile
$edit_profile_details = new \OpenAPI\Client\Model\EditProfileDetails(); // \OpenAPI\Client\Model\EditProfileDetails

try {
    $result = $apiInstance->editProfile($id, $edit_profile_details);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomisationProfilesApi->editProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Identifier of the profile | |
| **edit_profile_details** | [**\OpenAPI\Client\Model\EditProfileDetails**](../Model/EditProfileDetails.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Profile**](../Model/Profile.md)

### Authorization

[BearerAccessToken](../../README.md#BearerAccessToken)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProfile()`

```php
getProfile($id): \OpenAPI\Client\Model\Profile
```

Get a profile

Get a single profile by its id.<br/><br/>Must pass the <a href='https://documentation.finapi.io/access/Application-management.2763423767.html' target='_blank'>mandator admin client</a>'s access_token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomisationProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Identifier of the profile

try {
    $result = $apiInstance->getProfile($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomisationProfilesApi->getProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Identifier of the profile | |

### Return type

[**\OpenAPI\Client\Model\Profile**](../Model/Profile.md)

### Authorization

[BearerAccessToken](../../README.md#BearerAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProfiles()`

```php
getProfiles($order, $page, $per_page): \OpenAPI\Client\Model\ProfilesPage
```

Get profiles

Get all profiles.<br/><br/>Must pass the <a href='https://documentation.finapi.io/access/Application-management.2763423767.html' target='_blank'>mandator admin client</a>'s access_token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: BearerAccessToken
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomisationProfilesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order = createdAt,desc; // string | Determines the order of the results. You can order by <code>createdAt</code> field ascending or descending. The general format is <code>property[,asc|desc]</code>, with <code>asc</code> being the default value.The default order is <code>createdAt,asc</code>.
$page = 1; // int | Page to load
$per_page = 20; // int | The number of items on the page

try {
    $result = $apiInstance->getProfiles($order, $page, $per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomisationProfilesApi->getProfiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order** | **string**| Determines the order of the results. You can order by &lt;code&gt;createdAt&lt;/code&gt; field ascending or descending. The general format is &lt;code&gt;property[,asc|desc]&lt;/code&gt;, with &lt;code&gt;asc&lt;/code&gt; being the default value.The default order is &lt;code&gt;createdAt,asc&lt;/code&gt;. | [optional] |
| **page** | **int**| Page to load | [optional] [default to 1] |
| **per_page** | **int**| The number of items on the page | [optional] [default to 20] |

### Return type

[**\OpenAPI\Client\Model\ProfilesPage**](../Model/ProfilesPage.md)

### Authorization

[BearerAccessToken](../../README.md#BearerAccessToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
