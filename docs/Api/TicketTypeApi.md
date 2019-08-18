# UvdeskApi\TicketTypeApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiTicketType**](TicketTypeApi.md#deleteApiTicketType) | **DELETE** /ticket-type/{id}.json | Delete existing TicketType
[**getApiTicketTypes**](TicketTypeApi.md#getApiTicketTypes) | **GET** /ticket-types.json | Return a collection of TicketTypes
[**postApiTicketTypes**](TicketTypeApi.md#postApiTicketTypes) | **POST** /ticket-types.json | Add new TicketType
[**putApiTicketType**](TicketTypeApi.md#putApiTicketType) | **PUT** /ticket-type/{id}.json | Edit existing TicketType


# **deleteApiTicketType**
> deleteApiTicketType($id)

Delete existing TicketType

Delete existing TicketType

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketTypeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApiTicketType($id);
} catch (Exception $e) {
    echo 'Exception when calling TicketTypeApi->deleteApiTicketType: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiTicketTypes**
> object getApiTicketTypes($is_active, $sort, $page, $search)

Return a collection of TicketTypes

Return a collection of TicketTypes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketTypeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$is_active = "is_active_example"; // string | 0|1
$sort = "sort_example"; // string | 
$page = "page_example"; // string | 
$search = "search_example"; // string | search

try {
    $result = $apiInstance->getApiTicketTypes($is_active, $sort, $page, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketTypeApi->getApiTicketTypes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **is_active** | **string**| 0|1 | [optional]
 **sort** | **string**|  | [optional]
 **page** | **string**|  | [optional]
 **search** | **string**| search | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiTicketTypes**
> postApiTicketTypes($name, $description, $is_active)

Add new TicketType

Add new TicketType

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketTypeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | name
$description = "description_example"; // string | description
$is_active = "is_active_example"; // string | isActive values: 0|1  Note:will be 0 ,if not given

try {
    $apiInstance->postApiTicketTypes($name, $description, $is_active);
} catch (Exception $e) {
    echo 'Exception when calling TicketTypeApi->postApiTicketTypes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| name | [optional]
 **description** | **string**| description | [optional]
 **is_active** | **string**| isActive values: 0|1  Note:will be 0 ,if not given | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicketType**
> putApiTicketType($id, $name, $description, $is_active)

Edit existing TicketType

Edit existing TicketType

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketTypeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$name = "name_example"; // string | name
$description = "description_example"; // string | description
$is_active = "is_active_example"; // string | isActive values: 0|1  Note:will be 0 ,if not given

try {
    $apiInstance->putApiTicketType($id, $name, $description, $is_active);
} catch (Exception $e) {
    echo 'Exception when calling TicketTypeApi->putApiTicketType: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **name** | **string**| name | [optional]
 **description** | **string**| description | [optional]
 **is_active** | **string**| isActive values: 0|1  Note:will be 0 ,if not given | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

