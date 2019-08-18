# UvdeskApi\TodoApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiTodo**](TodoApi.md#deleteApiTodo) | **DELETE** /todo/{id}.json | Delete Todo
[**postApiTodo**](TodoApi.md#postApiTodo) | **POST** /todo.json | Add Todo
[**putApiTodo**](TodoApi.md#putApiTodo) | **PUT** /todo/{id}.json | Edit Todo


# **deleteApiTodo**
> deleteApiTodo($id, $task_id, $thread_id, $description, $status)

Delete Todo

Delete Todo

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TodoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$task_id = "task_id_example"; // string | for working on Task taskId is required
$thread_id = "thread_id_example"; // string | for working on Ticket ticketId is required
$description = "description_example"; // string | Desciption of Todo. required for POST Method
$status = "status_example"; // string | 0|1 for icncomplete|complete. default: 0 . required for PUT method

try {
    $apiInstance->deleteApiTodo($id, $task_id, $thread_id, $description, $status);
} catch (Exception $e) {
    echo 'Exception when calling TodoApi->deleteApiTodo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **task_id** | **string**| for working on Task taskId is required | [optional]
 **thread_id** | **string**| for working on Ticket ticketId is required | [optional]
 **description** | **string**| Desciption of Todo. required for POST Method | [optional]
 **status** | **string**| 0|1 for icncomplete|complete. default: 0 . required for PUT method | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiTodo**
> postApiTodo($task_id, $thread_id, $description, $status)

Add Todo

Add Todo

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TodoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$task_id = "task_id_example"; // string | for working on Task taskId is required
$thread_id = "thread_id_example"; // string | for working on Ticket ticketId is required
$description = "description_example"; // string | Desciption of Todo. required for POST Method
$status = "status_example"; // string | 0|1 for icncomplete|complete. default: 0 . required for PUT method

try {
    $apiInstance->postApiTodo($task_id, $thread_id, $description, $status);
} catch (Exception $e) {
    echo 'Exception when calling TodoApi->postApiTodo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | **string**| for working on Task taskId is required | [optional]
 **thread_id** | **string**| for working on Ticket ticketId is required | [optional]
 **description** | **string**| Desciption of Todo. required for POST Method | [optional]
 **status** | **string**| 0|1 for icncomplete|complete. default: 0 . required for PUT method | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTodo**
> putApiTodo($id, $task_id, $thread_id, $description, $status)

Edit Todo

Edit Todo

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TodoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$task_id = "task_id_example"; // string | for working on Task taskId is required
$thread_id = "thread_id_example"; // string | for working on Ticket ticketId is required
$description = "description_example"; // string | Desciption of Todo. required for POST Method
$status = "status_example"; // string | 0|1 for icncomplete|complete. default: 0 . required for PUT method

try {
    $apiInstance->putApiTodo($id, $task_id, $thread_id, $description, $status);
} catch (Exception $e) {
    echo 'Exception when calling TodoApi->putApiTodo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **task_id** | **string**| for working on Task taskId is required | [optional]
 **thread_id** | **string**| for working on Ticket ticketId is required | [optional]
 **description** | **string**| Desciption of Todo. required for POST Method | [optional]
 **status** | **string**| 0|1 for icncomplete|complete. default: 0 . required for PUT method | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

