# UvdeskApi\SavedReplyApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiSavedReply**](SavedReplyApi.md#deleteApiSavedReply) | **DELETE** /saved-reply/{template}.json | Delete existing savedReply
[**getApiSavedReplys**](SavedReplyApi.md#getApiSavedReplys) | **GET** /saved-replys.json | Returns a collection of SavedReply
[**postApiSavedReplys**](SavedReplyApi.md#postApiSavedReplys) | **POST** /saved-replys.json | Add reply
[**putApiSavedReply**](SavedReplyApi.md#putApiSavedReply) | **PUT** /saved-reply/{template}.json | edit reply


# **deleteApiSavedReply**
> deleteApiSavedReply($template, $sort, $page, $search)

Delete existing savedReply

Delete existing savedReply

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\SavedReplyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template = "template_example"; // string | 
$sort = "sort_example"; // string | 
$page = "page_example"; // string | 
$search = "search_example"; // string | search savedReply by name

try {
    $apiInstance->deleteApiSavedReply($template, $sort, $page, $search);
} catch (Exception $e) {
    echo 'Exception when calling SavedReplyApi->deleteApiSavedReply: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template** | **string**|  |
 **sort** | **string**|  | [optional]
 **page** | **string**|  | [optional]
 **search** | **string**| search savedReply by name | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiSavedReplys**
> object getApiSavedReplys($sort, $page, $search)

Returns a collection of SavedReply

Returns a collection of SavedReply

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\SavedReplyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sort = "sort_example"; // string | 
$page = "page_example"; // string | 
$search = "search_example"; // string | search savedReply by name

try {
    $result = $apiInstance->getApiSavedReplys($sort, $page, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SavedReplyApi->getApiSavedReplys: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort** | **string**|  | [optional]
 **page** | **string**|  | [optional]
 **search** | **string**| search savedReply by name | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiSavedReplys**
> postApiSavedReplys($name, $message)

Add reply

Add reply

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\SavedReplyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | name of reply
$message = "message_example"; // string | message (may be in html format)

try {
    $apiInstance->postApiSavedReplys($name, $message);
} catch (Exception $e) {
    echo 'Exception when calling SavedReplyApi->postApiSavedReplys: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| name of reply | [optional]
 **message** | **string**| message (may be in html format) | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiSavedReply**
> putApiSavedReply($template, $name, $message)

edit reply

edit reply

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\SavedReplyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template = "template_example"; // string | 
$name = "name_example"; // string | name of reply
$message = "message_example"; // string | message (may be in html format)

try {
    $apiInstance->putApiSavedReply($template, $name, $message);
} catch (Exception $e) {
    echo 'Exception when calling SavedReplyApi->putApiSavedReply: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template** | **string**|  |
 **name** | **string**| name of reply | [optional]
 **message** | **string**| message (may be in html format) | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

