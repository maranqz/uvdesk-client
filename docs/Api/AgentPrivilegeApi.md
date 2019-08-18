# UvdeskApi\AgentPrivilegeApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiAgentPrivilege**](AgentPrivilegeApi.md#deleteApiAgentPrivilege) | **DELETE** /agent-privilege/{id}.json | Delete existing privilege
[**getApiAgentPrivileges**](AgentPrivilegeApi.md#getApiAgentPrivileges) | **GET** /agent-privileges.json | View all privilege
[**postApiAgentPrivileges**](AgentPrivilegeApi.md#postApiAgentPrivileges) | **POST** /agent-privileges.json | Add privilege
[**putApiAgentPrivilege**](AgentPrivilegeApi.md#putApiAgentPrivilege) | **PUT** /agent-privilege/{id}.json | Add privilege


# **deleteApiAgentPrivilege**
> deleteApiAgentPrivilege($id)

Delete existing privilege

Delete existing privilege

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\AgentPrivilegeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApiAgentPrivilege($id);
} catch (Exception $e) {
    echo 'Exception when calling AgentPrivilegeApi->deleteApiAgentPrivilege: ', $e->getMessage(), PHP_EOL;
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

# **getApiAgentPrivileges**
> object getApiAgentPrivileges($sort, $search)

View all privilege

View all privilege

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\AgentPrivilegeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sort = "sort_example"; // string | 
$search = "search_example"; // string | search

try {
    $result = $apiInstance->getApiAgentPrivileges($sort, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AgentPrivilegeApi->getApiAgentPrivileges: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort** | **string**|  | [optional]
 **search** | **string**| search | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiAgentPrivileges**
> postApiAgentPrivileges($name, $description, $privileges)

Add privilege

Add privilege

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\AgentPrivilegeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | name
$description = "description_example"; // string | description
$privileges = "privileges_example"; // string | array of privileges required like ROLE_AGENT_CREATE_TASK

try {
    $apiInstance->postApiAgentPrivileges($name, $description, $privileges);
} catch (Exception $e) {
    echo 'Exception when calling AgentPrivilegeApi->postApiAgentPrivileges: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| name | [optional]
 **description** | **string**| description | [optional]
 **privileges** | **string**| array of privileges required like ROLE_AGENT_CREATE_TASK | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiAgentPrivilege**
> putApiAgentPrivilege($id, $name, $description, $privileges)

Add privilege

Add privilege

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\AgentPrivilegeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$name = "name_example"; // string | name
$description = "description_example"; // string | description
$privileges = "privileges_example"; // string | array of privileges required like ROLE_AGENT_CREATE_TASK

try {
    $apiInstance->putApiAgentPrivilege($id, $name, $description, $privileges);
} catch (Exception $e) {
    echo 'Exception when calling AgentPrivilegeApi->putApiAgentPrivilege: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **name** | **string**| name | [optional]
 **description** | **string**| description | [optional]
 **privileges** | **string**| array of privileges required like ROLE_AGENT_CREATE_TASK | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

