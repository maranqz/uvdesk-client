# UvdeskApi\MailboxApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiMailbox**](MailboxApi.md#deleteApiMailbox) | **DELETE** /mailbox/{id}.json | Delete Mailbox
[**getApiMailboxes**](MailboxApi.md#getApiMailboxes) | **GET** /mailboxes.json | Returns a collection of Mailboxes
[**postApiMailboxes**](MailboxApi.md#postApiMailboxes) | **POST** /mailboxes.json | Add Mailbox
[**putApiMailbox**](MailboxApi.md#putApiMailbox) | **PUT** /mailbox/{id}.json | Edit Mailbox


# **deleteApiMailbox**
> deleteApiMailbox($id, $name, $email)

Delete Mailbox

Delete Mailbox

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\MailboxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$name = "name_example"; // string | mailbox name
$email = "email_example"; // string | mailbox address

try {
    $apiInstance->deleteApiMailbox($id, $name, $email);
} catch (Exception $e) {
    echo 'Exception when calling MailboxApi->deleteApiMailbox: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **name** | **string**| mailbox name | [optional]
 **email** | **string**| mailbox address | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiMailboxes**
> object getApiMailboxes()

Returns a collection of Mailboxes

Returns a collection of Mailboxes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\MailboxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getApiMailboxes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MailboxApi->getApiMailboxes: ', $e->getMessage(), PHP_EOL;
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

# **postApiMailboxes**
> postApiMailboxes($name, $email)

Add Mailbox

Add Mailbox

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\MailboxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | mailbox name
$email = "email_example"; // string | mailbox address

try {
    $apiInstance->postApiMailboxes($name, $email);
} catch (Exception $e) {
    echo 'Exception when calling MailboxApi->postApiMailboxes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| mailbox name | [optional]
 **email** | **string**| mailbox address | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiMailbox**
> putApiMailbox($id, $name, $email)

Edit Mailbox

Edit Mailbox

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\MailboxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$name = "name_example"; // string | mailbox name
$email = "email_example"; // string | mailbox address

try {
    $apiInstance->putApiMailbox($id, $name, $email);
} catch (Exception $e) {
    echo 'Exception when calling MailboxApi->putApiMailbox: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **name** | **string**| mailbox name | [optional]
 **email** | **string**| mailbox address | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

