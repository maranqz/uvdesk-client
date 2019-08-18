# UvdeskApi\CustomerApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiCustomer**](CustomerApi.md#deleteApiCustomer) | **DELETE** /customer/{id}.json | delete a given customer
[**getApiCustomer**](CustomerApi.md#getApiCustomer) | **GET** /customer/{id}.json | View a customer
[**getApiCustomers**](CustomerApi.md#getApiCustomers) | **GET** /customers.json | Returns a collection of customers
[**patchApiCustomer**](CustomerApi.md#patchApiCustomer) | **PATCH** /customer/{id}.json | add/remove star to customer
[**postApiCustomers**](CustomerApi.md#postApiCustomers) | **POST** /customers.json | Add new Customer
[**putApiCustomer**](CustomerApi.md#putApiCustomer) | **PUT** /customer/{id}.json | edit existing customer


# **deleteApiCustomer**
> deleteApiCustomer($id)

delete a given customer

delete a given customer

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApiCustomer($id);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->deleteApiCustomer: ', $e->getMessage(), PHP_EOL;
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

# **getApiCustomer**
> object getApiCustomer($id)

View a customer

View a customer

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getApiCustomer($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->getApiCustomer: ', $e->getMessage(), PHP_EOL;
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

# **getApiCustomers**
> object getApiCustomers($starred, $is_active, $sort, $page, $search)

Returns a collection of customers

Returns a collection of customers

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$starred = "starred_example"; // string | 
$is_active = "is_active_example"; // string | 
$sort = "sort_example"; // string | 
$page = "page_example"; // string | 
$search = "search_example"; // string | search in all customer's name and email

try {
    $result = $apiInstance->getApiCustomers($starred, $is_active, $sort, $page, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->getApiCustomers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **starred** | **string**|  | [optional]
 **is_active** | **string**|  | [optional]
 **sort** | **string**|  | [optional]
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

# **patchApiCustomer**
> patchApiCustomer($id)

add/remove star to customer

add/remove star to customer

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->patchApiCustomer($id);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->patchApiCustomer: ', $e->getMessage(), PHP_EOL;
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

# **postApiCustomers**
> postApiCustomers($email, $first_name, $last_name)

Add new Customer

Add new Customer

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email = "email_example"; // string | email id
$first_name = "first_name_example"; // string | first name
$last_name = "last_name_example"; // string | last name

try {
    $apiInstance->postApiCustomers($email, $first_name, $last_name);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->postApiCustomers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **string**| email id | [optional]
 **first_name** | **string**| first name | [optional]
 **last_name** | **string**| last name | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiCustomer**
> putApiCustomer($id, $email, $first_name, $last_name)

edit existing customer

edit existing customer

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$email = "email_example"; // string | email id
$first_name = "first_name_example"; // string | first name
$last_name = "last_name_example"; // string | last name

try {
    $apiInstance->putApiCustomer($id, $email, $first_name, $last_name);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->putApiCustomer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **email** | **string**| email id | [optional]
 **first_name** | **string**| first name | [optional]
 **last_name** | **string**| last name | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

