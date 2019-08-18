# UvdeskApi\TeamsubgroupApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiSubGroup**](TeamsubgroupApi.md#deleteApiSubGroup) | **DELETE** /sub-group/{id}.json | Delete existing Subgroup
[**getApiSubGroups**](TeamsubgroupApi.md#getApiSubGroups) | **GET** /sub-groups.json | View Subgroups
[**postApiSubGroups**](TeamsubgroupApi.md#postApiSubGroups) | **POST** /sub-groups.json | Add Subgroup
[**putApiSubGroup**](TeamsubgroupApi.md#putApiSubGroup) | **PUT** /sub-group/{id}.json | modify Subgroup


# **deleteApiSubGroup**
> deleteApiSubGroup($id)

Delete existing Subgroup

Delete existing Subgroup

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TeamsubgroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApiSubGroup($id);
} catch (Exception $e) {
    echo 'Exception when calling TeamsubgroupApi->deleteApiSubGroup: ', $e->getMessage(), PHP_EOL;
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

# **getApiSubGroups**
> object getApiSubGroups($sort, $is_active, $search)

View Subgroups

View Subgroups

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TeamsubgroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sort = "sort_example"; // string | 
$is_active = "is_active_example"; // string | 0|1
$search = "search_example"; // string | search

try {
    $result = $apiInstance->getApiSubGroups($sort, $is_active, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsubgroupApi->getApiSubGroups: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort** | **string**|  | [optional]
 **is_active** | **string**| 0|1 | [optional]
 **search** | **string**| search | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiSubGroups**
> postApiSubGroups($name, $description, $groups, $users)

Add Subgroup

Add Subgroup

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TeamsubgroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | name
$description = "description_example"; // string | description
$groups = "groups_example"; // string | array of subgroup ids
$users = "users_example"; // string | array of users for subgroup/team

try {
    $apiInstance->postApiSubGroups($name, $description, $groups, $users);
} catch (Exception $e) {
    echo 'Exception when calling TeamsubgroupApi->postApiSubGroups: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| name | [optional]
 **description** | **string**| description | [optional]
 **groups** | **string**| array of subgroup ids | [optional]
 **users** | **string**| array of users for subgroup/team | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiSubGroup**
> putApiSubGroup($id, $name, $description, $groups, $users)

modify Subgroup

modify Subgroup

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TeamsubgroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$name = "name_example"; // string | name
$description = "description_example"; // string | description
$groups = "groups_example"; // string | array of subgroup ids
$users = "users_example"; // string | array of users for subgroup/team

try {
    $apiInstance->putApiSubGroup($id, $name, $description, $groups, $users);
} catch (Exception $e) {
    echo 'Exception when calling TeamsubgroupApi->putApiSubGroup: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **name** | **string**| name | [optional]
 **description** | **string**| description | [optional]
 **groups** | **string**| array of subgroup ids | [optional]
 **users** | **string**| array of users for subgroup/team | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

