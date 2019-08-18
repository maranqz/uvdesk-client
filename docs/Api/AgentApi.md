# UvdeskApi\AgentApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiMember**](AgentApi.md#deleteApiMember) | **DELETE** /member/{id}.json | Delete a given member
[**getApiMember**](AgentApi.md#getApiMember) | **GET** /member/{id}.json | View a member
[**getApiMembers**](AgentApi.md#getApiMembers) | **GET** /members.json | Return a collection of members
[**postApiMembers**](AgentApi.md#postApiMembers) | **POST** /members.json | Add new Member
[**putApiMember**](AgentApi.md#putApiMember) | **PUT** /member/{id}.json | edit existing member


# **deleteApiMember**
> deleteApiMember($id)

Delete a given member

Delete a given member

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\AgentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApiMember($id);
} catch (Exception $e) {
    echo 'Exception when calling AgentApi->deleteApiMember: ', $e->getMessage(), PHP_EOL;
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

# **getApiMember**
> object getApiMember($id)

View a member

View a member

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\AgentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getApiMember($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AgentApi->getApiMember: ', $e->getMessage(), PHP_EOL;
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

# **getApiMembers**
> object getApiMembers($starred, $is_active, $sort, $page, $search, $full_list)

Return a collection of members

Return a collection of members

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\AgentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$starred = "starred_example"; // string | 
$is_active = "is_active_example"; // string | 
$sort = "sort_example"; // string | 
$page = "page_example"; // string | 
$search = "search_example"; // string | search in all member's name and email
$full_list = "full_list_example"; // string | To get All members without pagination and with minimum data

try {
    $result = $apiInstance->getApiMembers($starred, $is_active, $sort, $page, $search, $full_list);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AgentApi->getApiMembers: ', $e->getMessage(), PHP_EOL;
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
 **search** | **string**| search in all member&#39;s name and email | [optional]
 **full_list** | **string**| To get All members without pagination and with minimum data | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiMembers**
> postApiMembers($first_name, $last_name, $email, $contact_number, $signature, $timezone, $password)

Add new Member

Add new Member

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\AgentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$first_name = "first_name_example"; // string | first name
$last_name = "last_name_example"; // string | last name
$email = "email_example"; // string | email
$contact_number = "contact_number_example"; // string | contact number
$signature = "signature_example"; // string | user's signature
$timezone = "timezone_example"; // string | timezone like Asia/Kolkata
$password = "password_example"; // string | provide password in form of array of 'first' and  'second'

try {
    $apiInstance->postApiMembers($first_name, $last_name, $email, $contact_number, $signature, $timezone, $password);
} catch (Exception $e) {
    echo 'Exception when calling AgentApi->postApiMembers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **first_name** | **string**| first name | [optional]
 **last_name** | **string**| last name | [optional]
 **email** | **string**| email | [optional]
 **contact_number** | **string**| contact number | [optional]
 **signature** | **string**| user&#39;s signature | [optional]
 **timezone** | **string**| timezone like Asia/Kolkata | [optional]
 **password** | **string**| provide password in form of array of &#39;first&#39; and  &#39;second&#39; | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiMember**
> putApiMember($id, $first_name, $last_name, $email, $contact_number, $signature, $timezone, $password)

edit existing member

edit existing member

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\AgentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$first_name = "first_name_example"; // string | first name
$last_name = "last_name_example"; // string | last name
$email = "email_example"; // string | email
$contact_number = "contact_number_example"; // string | contact number
$signature = "signature_example"; // string | user's signature
$timezone = "timezone_example"; // string | timezone like Asia/Kolkata
$password = "password_example"; // string | provide password in form of array of 'first' and  'second'

try {
    $apiInstance->putApiMember($id, $first_name, $last_name, $email, $contact_number, $signature, $timezone, $password);
} catch (Exception $e) {
    echo 'Exception when calling AgentApi->putApiMember: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **first_name** | **string**| first name | [optional]
 **last_name** | **string**| last name | [optional]
 **email** | **string**| email | [optional]
 **contact_number** | **string**| contact number | [optional]
 **signature** | **string**| user&#39;s signature | [optional]
 **timezone** | **string**| timezone like Asia/Kolkata | [optional]
 **password** | **string**| provide password in form of array of &#39;first&#39; and  &#39;second&#39; | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

