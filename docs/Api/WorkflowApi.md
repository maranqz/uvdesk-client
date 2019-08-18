# UvdeskApi\WorkflowApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiWorkflow**](WorkflowApi.md#deleteApiWorkflow) | **DELETE** /workflow/{type}/{id}.json | delete a given Workflow
[**getApiWorkflows**](WorkflowApi.md#getApiWorkflows) | **GET** /workflows.json | View workflow details
[**postApiWorkflows**](WorkflowApi.md#postApiWorkflows) | **POST** /workflows.json | Add Workflow
[**putApiWorkflow**](WorkflowApi.md#putApiWorkflow) | **PUT** /workflow/{type}/{id}.json | Edit Workflow
[**putApiWorkflowsOrder**](WorkflowApi.md#putApiWorkflowsOrder) | **PUT** /workflows/order.json | Reorder workflows


# **deleteApiWorkflow**
> deleteApiWorkflow($type, $id)

delete a given Workflow

delete a given Workflow

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\WorkflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$type = "type_example"; // string | 
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApiWorkflow($type, $id);
} catch (Exception $e) {
    echo 'Exception when calling WorkflowApi->deleteApiWorkflow: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **string**|  |
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiWorkflows**
> object getApiWorkflows()

View workflow details

View workflow details

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\WorkflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getApiWorkflows();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkflowApi->getApiWorkflows: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiWorkflows**
> postApiWorkflows($name, $type, $actions, $events, $conditions)

Add Workflow

Add Workflow

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\WorkflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | workflow name
$type = "type_example"; // string | workflow type 0|1 for manual|automatic
$actions = "actions_example"; // string | action(s) to be performed . Contains subfields: type , value. Actions must be given in assosiative array format
$events = "events_example"; // string | required for type:1 i.e. automatic. Events on which workflow to be triggered. Contains subfields: event , trigger .
$conditions = "conditions_example"; // string | conditions for workflow. Contains subfields: type, match, value .

try {
    $apiInstance->postApiWorkflows($name, $type, $actions, $events, $conditions);
} catch (Exception $e) {
    echo 'Exception when calling WorkflowApi->postApiWorkflows: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| workflow name | [optional]
 **type** | **string**| workflow type 0|1 for manual|automatic | [optional]
 **actions** | **string**| action(s) to be performed . Contains subfields: type , value. Actions must be given in assosiative array format | [optional]
 **events** | **string**| required for type:1 i.e. automatic. Events on which workflow to be triggered. Contains subfields: event , trigger . | [optional]
 **conditions** | **string**| conditions for workflow. Contains subfields: type, match, value . | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiWorkflow**
> putApiWorkflow($type, $id, $name, $actions, $events, $conditions)

Edit Workflow

Edit Workflow

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\WorkflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$type = "type_example"; // string | 
$id = 8.14; // float | 
$name = "name_example"; // string | workflow name
$actions = "actions_example"; // string | action(s) to be performed . Contains subfields: type , value. Actions must be given in assosiative array format
$events = "events_example"; // string | required for type:1 i.e. automatic. Events on which workflow to be triggered. Contains subfields: event , trigger .
$conditions = "conditions_example"; // string | conditions for workflow. Contains subfields: type, match, value .

try {
    $apiInstance->putApiWorkflow($type, $id, $name, $actions, $events, $conditions);
} catch (Exception $e) {
    echo 'Exception when calling WorkflowApi->putApiWorkflow: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **string**|  |
 **id** | **float**|  |
 **name** | **string**| workflow name | [optional]
 **actions** | **string**| action(s) to be performed . Contains subfields: type , value. Actions must be given in assosiative array format | [optional]
 **events** | **string**| required for type:1 i.e. automatic. Events on which workflow to be triggered. Contains subfields: event , trigger . | [optional]
 **conditions** | **string**| conditions for workflow. Contains subfields: type, match, value . | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiWorkflowsOrder**
> putApiWorkflowsOrder($auto)

Reorder workflows

Reorder workflows

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\WorkflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$auto = "auto_example"; // string | assosiative array , in format workflow-id:position

try {
    $apiInstance->putApiWorkflowsOrder($auto);
} catch (Exception $e) {
    echo 'Exception when calling WorkflowApi->putApiWorkflowsOrder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auto** | **string**| assosiative array , in format workflow-id:position | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

