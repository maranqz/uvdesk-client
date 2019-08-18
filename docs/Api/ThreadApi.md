# UvdeskApi\ThreadApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiTicketThread**](ThreadApi.md#deleteApiTicketThread) | **DELETE** /ticket/{ticketId}/thread/{id}.json | DELETE thread
[**getApiTicketThreads**](ThreadApi.md#getApiTicketThreads) | **GET** /ticket/{id}/threads.json | Returns a collection of threads
[**patchApiTicketThread**](ThreadApi.md#patchApiTicketThread) | **PATCH** /ticket/{ticketId}/thread/{id}.json | lock/unlock thread
[**postApiTicketThreads**](ThreadApi.md#postApiTicketThreads) | **POST** /ticket/{id}/threads.json | Add new Thread
[**putApiTicketThread**](ThreadApi.md#putApiTicketThread) | **PUT** /ticket/{ticketId}/thread/{id}.json | Edit existing thread


# **deleteApiTicketThread**
> deleteApiTicketThread($ticket_id, $id)

DELETE thread

DELETE thread

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\ThreadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ticket_id = "ticket_id_example"; // string | 
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApiTicketThread($ticket_id, $id);
} catch (Exception $e) {
    echo 'Exception when calling ThreadApi->deleteApiTicketThread: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticket_id** | **string**|  |
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiTicketThreads**
> object getApiTicketThreads($id)

Returns a collection of threads

Returns a collection of threads

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\ThreadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getApiTicketThreads($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ThreadApi->getApiTicketThreads: ', $e->getMessage(), PHP_EOL;
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

# **patchApiTicketThread**
> patchApiTicketThread($ticket_id, $id)

lock/unlock thread

lock/unlock thread

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\ThreadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ticket_id = "ticket_id_example"; // string | 
$id = "id_example"; // string | 

try {
    $apiInstance->patchApiTicketThread($ticket_id, $id);
} catch (Exception $e) {
    echo 'Exception when calling ThreadApi->patchApiTicketThread: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticket_id** | **string**|  |
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiTicketThreads**
> postApiTicketThreads($id, $thread_type, $reply, $status, $to, $files, $act_as_type, $act_as_email)

Add new Thread

Add new Thread

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\ThreadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$thread_type = "thread_type_example"; // string | threadtype: reply|forward|note
$reply = "reply_example"; // string | main content of thread
$status = "status_example"; // string | status id value: 1|2|3|4|5|6 for open|pending|resolved|closed|Spam|Answered repectively
$to = "to_example"; // string | to in case of threadType:forward
$files = "files_example"; // string | attachements
$act_as_type = "act_as_type_example"; // string | admin can actAsType customer, agent
$act_as_email = "act_as_email_example"; // string | provide with actAsType

try {
    $apiInstance->postApiTicketThreads($id, $thread_type, $reply, $status, $to, $files, $act_as_type, $act_as_email);
} catch (Exception $e) {
    echo 'Exception when calling ThreadApi->postApiTicketThreads: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **thread_type** | **string**| threadtype: reply|forward|note | [optional]
 **reply** | **string**| main content of thread | [optional]
 **status** | **string**| status id value: 1|2|3|4|5|6 for open|pending|resolved|closed|Spam|Answered repectively | [optional]
 **to** | **string**| to in case of threadType:forward | [optional]
 **files** | **string**| attachements | [optional]
 **act_as_type** | **string**| admin can actAsType customer, agent | [optional]
 **act_as_email** | **string**| provide with actAsType | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicketThread**
> putApiTicketThread($ticket_id, $id, $reply)

Edit existing thread

Edit existing thread

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\ThreadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ticket_id = "ticket_id_example"; // string | 
$id = "id_example"; // string | 
$reply = "reply_example"; // string | main content of thread

try {
    $apiInstance->putApiTicketThread($ticket_id, $id, $reply);
} catch (Exception $e) {
    echo 'Exception when calling ThreadApi->putApiTicketThread: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticket_id** | **string**|  |
 **id** | **string**|  |
 **reply** | **string**| main content of thread | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

