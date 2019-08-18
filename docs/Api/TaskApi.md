# UvdeskApi\TaskApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiTask**](TaskApi.md#deleteApiTask) | **DELETE** /task/{id}.json | Delete existing task
[**deleteApiTaskFollower**](TaskApi.md#deleteApiTaskFollower) | **DELETE** /task/{id}/follower.json | Remove Follower
[**deleteApiTaskThread**](TaskApi.md#deleteApiTaskThread) | **DELETE** /task/{id}/thread.json | remove thread
[**getApiTask**](TaskApi.md#getApiTask) | **GET** /task/{id}.json | View a Task
[**getApiTasks**](TaskApi.md#getApiTasks) | **GET** /tasks.json | Returns a collection of Tasks
[**postApiTaskFollower**](TaskApi.md#postApiTaskFollower) | **POST** /task/{id}/follower.json | add Follower
[**postApiTaskThread**](TaskApi.md#postApiTaskThread) | **POST** /task/{id}/thread.json | add thread
[**postApiTasks**](TaskApi.md#postApiTasks) | **POST** /tasks.json | Add new Task
[**putApiTask**](TaskApi.md#putApiTask) | **PUT** /task/{id}.json | update existing task


# **deleteApiTask**
> deleteApiTask($id)

Delete existing task

Delete existing task

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApiTask($id);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->deleteApiTask: ', $e->getMessage(), PHP_EOL;
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

# **deleteApiTaskFollower**
> deleteApiTaskFollower($id, $follower_id)

Remove Follower

Remove Follower

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$follower_id = "follower_id_example"; // string | followerId

try {
    $apiInstance->deleteApiTaskFollower($id, $follower_id);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->deleteApiTaskFollower: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **follower_id** | **string**| followerId | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteApiTaskThread**
> deleteApiTaskThread($id, $description, $stage)

remove thread

remove thread

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$description = "description_example"; // string | description
$stage = "stage_example"; // string | stage Id

try {
    $apiInstance->deleteApiTaskThread($id, $description, $stage);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->deleteApiTaskThread: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **description** | **string**| description | [optional]
 **stage** | **string**| stage Id | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiTask**
> object getApiTask($id)

View a Task

View a Task

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getApiTask($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->getApiTask: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiTasks**
> object getApiTasks($sort, $stage, $priority, $page, $search)

Returns a collection of Tasks

Returns a collection of Tasks

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sort = "sort_example"; // string | 
$stage = 56; // int | stageId 1|2|3 for New|in Progress|Done
$priority = 56; // int | value: 1|2|3|4 for Low|medium|High|Urgent
$page = "page_example"; // string | 
$search = "search_example"; // string | search in all customer's name and email

try {
    $result = $apiInstance->getApiTasks($sort, $stage, $priority, $page, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->getApiTasks: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort** | **string**|  | [optional]
 **stage** | **int**| stageId 1|2|3 for New|in Progress|Done | [optional]
 **priority** | **int**| value: 1|2|3|4 for Low|medium|High|Urgent | [optional]
 **page** | **string**|  | [optional]
 **search** | **string**| search in all customer&#39;s name and email | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiTaskFollower**
> postApiTaskFollower($id, $follower_id)

add Follower

add Follower

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$follower_id = "follower_id_example"; // string | followerId

try {
    $apiInstance->postApiTaskFollower($id, $follower_id);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postApiTaskFollower: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **follower_id** | **string**| followerId | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiTaskThread**
> postApiTaskThread($id, $description, $stage)

add thread

add thread

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$description = "description_example"; // string | description
$stage = "stage_example"; // string | stage Id

try {
    $apiInstance->postApiTaskThread($id, $description, $stage);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postApiTaskThread: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **description** | **string**| description | [optional]
 **stage** | **string**| stage Id | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiTasks**
> postApiTasks($subject, $description, $assigned_agent, $deadline, $ticket, $thread_ids)

Add new Task

Add new Task

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subject = "subject_example"; // string | task subject
$description = "description_example"; // string | task description
$assigned_agent = "assigned_agent_example"; // string | assignedAgent id
$deadline = "deadline_example"; // string | task deadline
$ticket = "ticket_example"; // string | ticket Id
$thread_ids = "thread_ids_example"; // string | array of threadIds

try {
    $apiInstance->postApiTasks($subject, $description, $assigned_agent, $deadline, $ticket, $thread_ids);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->postApiTasks: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subject** | **string**| task subject | [optional]
 **description** | **string**| task description | [optional]
 **assigned_agent** | **string**| assignedAgent id | [optional]
 **deadline** | **string**| task deadline | [optional]
 **ticket** | **string**| ticket Id | [optional]
 **thread_ids** | **string**| array of threadIds | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTask**
> putApiTask($id, $priority, $stage, $subject, $assigned_agent, $description)

update existing task

update existing task

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$priority = "priority_example"; // string | priority id
$stage = "stage_example"; // string | stage id
$subject = "subject_example"; // string | subject
$assigned_agent = "assigned_agent_example"; // string | assignedAgent id
$description = "description_example"; // string | description

try {
    $apiInstance->putApiTask($id, $priority, $stage, $subject, $assigned_agent, $description);
} catch (Exception $e) {
    echo 'Exception when calling TaskApi->putApiTask: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **priority** | **string**| priority id | [optional]
 **stage** | **string**| stage id | [optional]
 **subject** | **string**| subject | [optional]
 **assigned_agent** | **string**| assignedAgent id | [optional]
 **description** | **string**| description | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

