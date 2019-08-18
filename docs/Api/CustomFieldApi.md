# UvdeskApi\CustomFieldApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiCustomField**](CustomFieldApi.md#deleteApiCustomField) | **DELETE** /custom-field/{field}.json | delete existing custom-field
[**getApiCustomFields**](CustomFieldApi.md#getApiCustomFields) | **GET** /custom-fields.json | Returns a collection of custom-fields
[**postApiCustomFields**](CustomFieldApi.md#postApiCustomFields) | **POST** /custom-fields.json | Add custom-field
[**putApiCustomField**](CustomFieldApi.md#putApiCustomField) | **PUT** /custom-field/{field}.json | Edit custom-field
[**putApiCustomFieldOrder**](CustomFieldApi.md#putApiCustomFieldOrder) | **PUT** /custom-field/order.json | Reorder CustomFields


# **deleteApiCustomField**
> deleteApiCustomField($field)

delete existing custom-field

delete existing custom-field

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomFieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$field = "field_example"; // string | 

try {
    $apiInstance->deleteApiCustomField($field);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldApi->deleteApiCustomField: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **field** | **string**|  |

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiCustomFields**
> object getApiCustomFields($sort, $page, $search)

Returns a collection of custom-fields

Returns a collection of custom-fields

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomFieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sort = "sort_example"; // string | 
$page = "page_example"; // string | 
$search = "search_example"; // string | search in custom-field names

try {
    $result = $apiInstance->getApiCustomFields($sort, $page, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldApi->getApiCustomFields: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort** | **string**|  | [optional]
 **page** | **string**|  | [optional]
 **search** | **string**| search in custom-field names | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiCustomFields**
> postApiCustomFields($name, $agent_type, $field_type, $sort_order, $dependency, $value, $status, $required)

Add custom-field

Add custom-field

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomFieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | custom field name
$agent_type = "agent_type_example"; // string | options: customer,agent, both . To add customfield for customer or agent
$field_type = "field_type_example"; // string | fieldType value like textarea, radio
$sort_order = "sort_order_example"; // string | sort order of custom-field
$dependency = "dependency_example"; // string | array of groups
$value = "value_example"; // string | custom-field placeholder value to added in custom field
$status = "status_example"; // string | custom-field active status
$required = "required_example"; // string | is custom-field required?

try {
    $apiInstance->postApiCustomFields($name, $agent_type, $field_type, $sort_order, $dependency, $value, $status, $required);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldApi->postApiCustomFields: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| custom field name | [optional]
 **agent_type** | **string**| options: customer,agent, both . To add customfield for customer or agent | [optional]
 **field_type** | **string**| fieldType value like textarea, radio | [optional]
 **sort_order** | **string**| sort order of custom-field | [optional]
 **dependency** | **string**| array of groups | [optional]
 **value** | **string**| custom-field placeholder value to added in custom field | [optional]
 **status** | **string**| custom-field active status | [optional]
 **required** | **string**| is custom-field required? | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiCustomField**
> putApiCustomField($field, $name, $agent_type, $field_type, $sort_order, $dependency, $value, $status, $required)

Edit custom-field

edit custom-field

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomFieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$field = "field_example"; // string | 
$name = "name_example"; // string | custom field name
$agent_type = "agent_type_example"; // string | options: customer,agent, both . To add customfield for customer or agent
$field_type = "field_type_example"; // string | fieldType value like textarea, radio
$sort_order = "sort_order_example"; // string | sort order of custom-field
$dependency = "dependency_example"; // string | array of groups
$value = "value_example"; // string | custom-field placeholder value to added in custom field
$status = "status_example"; // string | custom-field active status
$required = "required_example"; // string | is custom-field required?

try {
    $apiInstance->putApiCustomField($field, $name, $agent_type, $field_type, $sort_order, $dependency, $value, $status, $required);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldApi->putApiCustomField: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **field** | **string**|  |
 **name** | **string**| custom field name | [optional]
 **agent_type** | **string**| options: customer,agent, both . To add customfield for customer or agent | [optional]
 **field_type** | **string**| fieldType value like textarea, radio | [optional]
 **sort_order** | **string**| sort order of custom-field | [optional]
 **dependency** | **string**| array of groups | [optional]
 **value** | **string**| custom-field placeholder value to added in custom field | [optional]
 **status** | **string**| custom-field active status | [optional]
 **required** | **string**| is custom-field required? | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiCustomFieldOrder**
> putApiCustomFieldOrder($sortorder)

Reorder CustomFields

Reorder CustomFields

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomFieldApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sortorder = "sortorder_example"; // string | assosiative array , in format customField-id:position

try {
    $apiInstance->putApiCustomFieldOrder($sortorder);
} catch (Exception $e) {
    echo 'Exception when calling CustomFieldApi->putApiCustomFieldOrder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sortorder** | **string**| assosiative array , in format customField-id:position | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

