# UvdeskApi\TicketApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiTicket**](TicketApi.md#deleteApiTicket) | **DELETE** /ticket/{id}.json | Delete a given ticket
[**deleteApiTicketCollaborator**](TicketApi.md#deleteApiTicketCollaborator) | **DELETE** /ticket/{id}/collaborator.json | Remove collaborator from Ticket
[**getApiTicket**](TicketApi.md#getApiTicket) | **GET** /ticket/{id}.json | View a ticket
[**getApiTicketAttachment**](TicketApi.md#getApiTicketAttachment) | **GET** /ticket/attachment/{id}.json | download attachment
[**patchApiTicket**](TicketApi.md#patchApiTicket) | **PATCH** /ticket/{id}.json | Edit given ticket&#39;s properties
[**postApiTicketCollaborator**](TicketApi.md#postApiTicketCollaborator) | **POST** /ticket/{id}/collaborator.json | Add collaborator for Ticket
[**putApiTicket**](TicketApi.md#putApiTicket) | **PUT** /ticket/{id}.json | Edit given ticket


# **deleteApiTicket**
> deleteApiTicket($id)

Delete a given ticket

Delete a given ticket

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteApiTicket($id);
} catch (Exception $e) {
    echo 'Exception when calling TicketApi->deleteApiTicket: ', $e->getMessage(), PHP_EOL;
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

# **deleteApiTicketCollaborator**
> deleteApiTicketCollaborator($id, $collaborator_id)

Remove collaborator from Ticket

Remove collaborator from Ticket

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$collaborator_id = "collaborator_id_example"; // string | collaborator's Id

try {
    $apiInstance->deleteApiTicketCollaborator($id, $collaborator_id);
} catch (Exception $e) {
    echo 'Exception when calling TicketApi->deleteApiTicketCollaborator: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **collaborator_id** | **string**| collaborator&#39;s Id | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiTicket**
> object getApiTicket($id)

View a ticket

View a ticket

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | This api uses ticket IncrementId, while all other uses ticket id

try {
    $result = $apiInstance->getApiTicket($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketApi->getApiTicket: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| This api uses ticket IncrementId, while all other uses ticket id |

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiTicketAttachment**
> object getApiTicketAttachment($id)

download attachment

download attachment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getApiTicketAttachment($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketApi->getApiTicketAttachment: ', $e->getMessage(), PHP_EOL;
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

# **patchApiTicket**
> patchApiTicket($id, $edit_type, $value)

Edit given ticket's properties

Edit given ticket's properties

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$edit_type = "edit_type_example"; // string | property type that you want to edit. options : status|type|priority|group|label|star
$value = "value_example"; // string | value for corresponding property, optional for editType:star

try {
    $apiInstance->patchApiTicket($id, $edit_type, $value);
} catch (Exception $e) {
    echo 'Exception when calling TicketApi->patchApiTicket: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **edit_type** | **string**| property type that you want to edit. options : status|type|priority|group|label|star | [optional]
 **value** | **string**| value for corresponding property, optional for editType:star | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiTicketCollaborator**
> postApiTicketCollaborator($id, $email)

Add collaborator for Ticket

Add collaborator for Ticket

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$email = "email_example"; // string | collaborator email

try {
    $apiInstance->postApiTicketCollaborator($id, $email);
} catch (Exception $e) {
    echo 'Exception when calling TicketApi->postApiTicketCollaborator: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **email** | **string**| collaborator email | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicket**
> putApiTicket($id, $type, $from, $reply, $subject)

Edit given ticket

Edit given ticket

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$type = "type_example"; // string | 1|2|3|4|5|6 for open|pending|resolved|closed|Spam|Answered repectively
$from = "from_example"; // string | email address
$reply = "reply_example"; // string | reply content
$subject = "subject_example"; // string | ticket subject

try {
    $apiInstance->putApiTicket($id, $type, $from, $reply, $subject);
} catch (Exception $e) {
    echo 'Exception when calling TicketApi->putApiTicket: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **type** | **string**| 1|2|3|4|5|6 for open|pending|resolved|closed|Spam|Answered repectively | [optional]
 **from** | **string**| email address | [optional]
 **reply** | **string**| reply content | [optional]
 **subject** | **string**| ticket subject | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

