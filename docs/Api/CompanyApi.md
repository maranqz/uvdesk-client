# UvdeskApi\CompanyApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getApiCompanySpam**](CompanyApi.md#getApiCompanySpam) | **GET** /company/spam.json | View company spam setting
[**putApiCompany**](CompanyApi.md#putApiCompany) | **PUT** /company.json | edit company details
[**putApiCompanySpam**](CompanyApi.md#putApiCompanySpam) | **PUT** /company/spam.json | edit Spam setting of company
[**putApiCompanyTheme**](CompanyApi.md#putApiCompanyTheme) | **PUT** /company/theme.json | edit theme of company


# **getApiCompanySpam**
> object getApiCompanySpam()

View company spam setting

View company spam setting

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CompanyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getApiCompanySpam();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CompanyApi->getApiCompanySpam: ', $e->getMessage(), PHP_EOL;
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

# **putApiCompany**
> putApiCompany($name, $support_email, $next_ticket_id, $timezone, $pending_since, $default_mailbox, $default_status, $default_priority, $time_format, $pending_notification_email_template)

edit company details

edit company details

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CompanyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | support name
$support_email = "support_email_example"; // string | support email id
$next_ticket_id = "next_ticket_id_example"; // string | it should be kept greater than last ticket id
$timezone = "timezone_example"; // string | timezone like Asia/Kolkata
$pending_since = "pending_since_example"; // string | no. of hours since customer last replied, to disable set to 0
$default_mailbox = "default_mailbox_example"; // string | mailbox id
$default_status = "default_status_example"; // string | default status
$default_priority = "default_priority_example"; // string | default priority
$time_format = "time_format_example"; // string | time format like m-d-y G:i
$pending_notification_email_template = "pending_notification_email_template_example"; // string | EmailTemplate of pending Notification

try {
    $apiInstance->putApiCompany($name, $support_email, $next_ticket_id, $timezone, $pending_since, $default_mailbox, $default_status, $default_priority, $time_format, $pending_notification_email_template);
} catch (Exception $e) {
    echo 'Exception when calling CompanyApi->putApiCompany: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| support name | [optional]
 **support_email** | **string**| support email id | [optional]
 **next_ticket_id** | **string**| it should be kept greater than last ticket id | [optional]
 **timezone** | **string**| timezone like Asia/Kolkata | [optional]
 **pending_since** | **string**| no. of hours since customer last replied, to disable set to 0 | [optional]
 **default_mailbox** | **string**| mailbox id | [optional]
 **default_status** | **string**| default status | [optional]
 **default_priority** | **string**| default priority | [optional]
 **time_format** | **string**| time format like m-d-y G:i | [optional]
 **pending_notification_email_template** | **string**| EmailTemplate of pending Notification | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiCompanySpam**
> putApiCompanySpam($black_list, $white_list)

edit Spam setting of company

edit Spam setting of company

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CompanyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$black_list = "black_list_example"; // string | blacklist
$white_list = "white_list_example"; // string | whiteList

try {
    $apiInstance->putApiCompanySpam($black_list, $white_list);
} catch (Exception $e) {
    echo 'Exception when calling CompanyApi->putApiCompanySpam: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **black_list** | **string**| blacklist | [optional]
 **white_list** | **string**| whiteList | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiCompanyTheme**
> putApiCompanyTheme($name, $domain, $c_name, $status, $logo, $favicon, $banner, $custom_css, $page_background_color, $header_background_color, $nav_text_color, $link_color, $link_hover_color, $article_text_color, $script, $site_descritption, $meta_description, $meta_keywords, $homepage_content, $ticket_create_option)

edit theme of company

edit theme of company

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\CompanyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | company Name
$domain = "domain_example"; // string | domain name of website like webkul
$c_name = "c_name_example"; // string | website name
$status = "status_example"; // string | 0|1 for deactivated|activated
$logo = "logo_example"; // string | Jpg, Jpeg, Png images are allowed. (50x50 px)
$favicon = "favicon_example"; // string | Jpg, Jpeg, Png images are allowed. (50x50 px)
$banner = "banner_example"; // string | Jpg, Jpeg, Png images are allowed. (50x50 px)
$custom_css = "custom_css_example"; // string | css file
$page_background_color = "page_background_color_example"; // string | page background color of theme
$header_background_color = "header_background_color_example"; // string | header background color of theme
$nav_text_color = "nav_text_color_example"; // string | navigation background color
$link_color = "link_color_example"; // string | link color of theme
$link_hover_color = "link_hover_color_example"; // string | link hover color for theme
$article_text_color = "article_text_color_example"; // string | article text color for theme
$script = "script_example"; // string | any required script fot theme
$site_descritption = "site_descritption_example"; // string | site description
$meta_description = "meta_description_example"; // string | meta description
$meta_keywords = "meta_keywords_example"; // string | meta keywords to describe content on website
$homepage_content = "homepage_content_example"; // string | home page content category|article
$ticket_create_option = "ticket_create_option_example"; // string | if login required to create tickets

try {
    $apiInstance->putApiCompanyTheme($name, $domain, $c_name, $status, $logo, $favicon, $banner, $custom_css, $page_background_color, $header_background_color, $nav_text_color, $link_color, $link_hover_color, $article_text_color, $script, $site_descritption, $meta_description, $meta_keywords, $homepage_content, $ticket_create_option);
} catch (Exception $e) {
    echo 'Exception when calling CompanyApi->putApiCompanyTheme: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| company Name | [optional]
 **domain** | **string**| domain name of website like webkul | [optional]
 **c_name** | **string**| website name | [optional]
 **status** | **string**| 0|1 for deactivated|activated | [optional]
 **logo** | **string**| Jpg, Jpeg, Png images are allowed. (50x50 px) | [optional]
 **favicon** | **string**| Jpg, Jpeg, Png images are allowed. (50x50 px) | [optional]
 **banner** | **string**| Jpg, Jpeg, Png images are allowed. (50x50 px) | [optional]
 **custom_css** | **string**| css file | [optional]
 **page_background_color** | **string**| page background color of theme | [optional]
 **header_background_color** | **string**| header background color of theme | [optional]
 **nav_text_color** | **string**| navigation background color | [optional]
 **link_color** | **string**| link color of theme | [optional]
 **link_hover_color** | **string**| link hover color for theme | [optional]
 **article_text_color** | **string**| article text color for theme | [optional]
 **script** | **string**| any required script fot theme | [optional]
 **site_descritption** | **string**| site description | [optional]
 **meta_description** | **string**| meta description | [optional]
 **meta_keywords** | **string**| meta keywords to describe content on website | [optional]
 **homepage_content** | **string**| home page content category|article | [optional]
 **ticket_create_option** | **string**| if login required to create tickets | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

