# UvdeskApi\FilterApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getApiFilters**](FilterApi.md#getApiFilters) | **GET** /filters.json | Get filter data


# **getApiFilters**
> object getApiFilters($group, $usergroup, $team, $type, $priority, $tag, $mailbox, $agent, $customer, $source, $userdata)

Get filter data

Get filter data

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\FilterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group = 56; // int | to get group data
$usergroup = 56; // int | to get group data with corresponding subgroups
$team = 56; // int | to get team data
$type = 56; // int | to get type data
$priority = 56; // int | to get priority data
$tag = 56; // int | to get tag data
$mailbox = 56; // int | to get mailbox data
$agent = 56; // int | to get agent data
$customer = 56; // int | to get customer data
$source = 56; // int | to get source data
$userdata = 56; // int | to get current user's data like roles

try {
    $result = $apiInstance->getApiFilters($group, $usergroup, $team, $type, $priority, $tag, $mailbox, $agent, $customer, $source, $userdata);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FilterApi->getApiFilters: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group** | **int**| to get group data | [optional]
 **usergroup** | **int**| to get group data with corresponding subgroups | [optional]
 **team** | **int**| to get team data | [optional]
 **type** | **int**| to get type data | [optional]
 **priority** | **int**| to get priority data | [optional]
 **tag** | **int**| to get tag data | [optional]
 **mailbox** | **int**| to get mailbox data | [optional]
 **agent** | **int**| to get agent data | [optional]
 **customer** | **int**| to get customer data | [optional]
 **source** | **int**| to get source data | [optional]
 **userdata** | **int**| to get current user&#39;s data like roles | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

