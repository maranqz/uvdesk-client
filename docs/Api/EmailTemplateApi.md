# UvdeskApi\EmailTemplateApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiEmailTemplate**](EmailTemplateApi.md#deleteApiEmailTemplate) | **DELETE** /email-template/{template}.json | Delete email-Template
[**getApiEmailTemplates**](EmailTemplateApi.md#getApiEmailTemplates) | **GET** /email-templates.json | Returns a collection of Email-Templates
[**postApiEmailTemplates**](EmailTemplateApi.md#postApiEmailTemplates) | **POST** /email-templates.json | Add email-template
[**putApiEmailTemplate**](EmailTemplateApi.md#putApiEmailTemplate) | **PUT** /email-template/{template}.json | Edit email-template


# **deleteApiEmailTemplate**
> deleteApiEmailTemplate($template, $sort, $page, $search)

Delete email-Template

Delete email-Template

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template = "template_example"; // string | 
$sort = "sort_example"; // string | 
$page = "page_example"; // string | 
$search = "search_example"; // string | search email-Templates by name

try {
    $apiInstance->deleteApiEmailTemplate($template, $sort, $page, $search);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->deleteApiEmailTemplate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template** | **string**|  |
 **sort** | **string**|  | [optional]
 **page** | **string**|  | [optional]
 **search** | **string**| search email-Templates by name | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiEmailTemplates**
> object getApiEmailTemplates($sort, $page, $search)

Returns a collection of Email-Templates

Returns a collection of Email-Templates

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sort = "sort_example"; // string | 
$page = "page_example"; // string | 
$search = "search_example"; // string | search email-Templates by name

try {
    $result = $apiInstance->getApiEmailTemplates($sort, $page, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->getApiEmailTemplates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort** | **string**|  | [optional]
 **page** | **string**|  | [optional]
 **search** | **string**| search email-Templates by name | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiEmailTemplates**
> postApiEmailTemplates($name, $subject, $message)

Add email-template

Add email-template

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | name of reply
$subject = "subject_example"; // string | subject of reply
$message = "message_example"; // string | message (may be in html format, can contain placeholders like {%ticket.id%})

try {
    $apiInstance->postApiEmailTemplates($name, $subject, $message);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->postApiEmailTemplates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| name of reply | [optional]
 **subject** | **string**| subject of reply | [optional]
 **message** | **string**| message (may be in html format, can contain placeholders like {%ticket.id%}) | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiEmailTemplate**
> putApiEmailTemplate($template, $name, $subject, $message)

Edit email-template

Edit email-template

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template = "template_example"; // string | 
$name = "name_example"; // string | name of reply
$subject = "subject_example"; // string | subject of reply
$message = "message_example"; // string | message (may be in html format, can contain placeholders like {%ticket.id%})

try {
    $apiInstance->putApiEmailTemplate($template, $name, $subject, $message);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->putApiEmailTemplate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template** | **string**|  |
 **name** | **string**| name of reply | [optional]
 **subject** | **string**| subject of reply | [optional]
 **message** | **string**| message (may be in html format, can contain placeholders like {%ticket.id%}) | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

