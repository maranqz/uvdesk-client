# UvdeskApi\TicketsApi

All URIs are relative to *https://subdomain.uvdesk.com/en/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteApiTicketTags**](TicketsApi.md#deleteApiTicketTags) | **DELETE** /ticket/{id}/tags.json | delete Tag from Ticket
[**deleteApiTickets**](TicketsApi.md#deleteApiTickets) | **DELETE** /tickets.json | Delete multiple Tickets
[**getApiTickets**](TicketsApi.md#getApiTickets) | **GET** /tickets.json | Return a Collection of Tickets
[**postApiTicketTags**](TicketsApi.md#postApiTicketTags) | **POST** /ticket/{id}/tags.json | Add Tag from Ticket
[**postApiTickets**](TicketsApi.md#postApiTickets) | **POST** /tickets.json | Add ticket
[**putApiTicketsAgent**](TicketsApi.md#putApiTicketsAgent) | **PUT** /tickets/agent.json | Assign Agent to multiple Tickets
[**putApiTicketsGroup**](TicketsApi.md#putApiTicketsGroup) | **PUT** /tickets/group.json | change Group of multiple Tickets
[**putApiTicketsLabel**](TicketsApi.md#putApiTicketsLabel) | **PUT** /tickets/label.json | add label to multiple Tickets
[**putApiTicketsPriority**](TicketsApi.md#putApiTicketsPriority) | **PUT** /tickets/priority.json | change Priority of multiple Tickets
[**putApiTicketsRestore**](TicketsApi.md#putApiTicketsRestore) | **PUT** /tickets/restore.json | Restore multiple Tickets
[**putApiTicketsStatus**](TicketsApi.md#putApiTicketsStatus) | **PUT** /tickets/status.json | change Status of multiple Tickets
[**putApiTicketsTrash**](TicketsApi.md#putApiTicketsTrash) | **PUT** /tickets/trash.json | Trash multiple Tickets


# **deleteApiTicketTags**
> deleteApiTicketTags($id, $name)

delete Tag from Ticket

delete Tag from Ticket

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$name = "name_example"; // string | tagname required for POST

try {
    $apiInstance->deleteApiTicketTags($id, $name);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->deleteApiTicketTags: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **name** | **string**| tagname required for POST | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteApiTickets**
> deleteApiTickets($ids)

Delete multiple Tickets

Delete multiple Tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ids = "ids_example"; // string | ticket ids to be deleted

try {
    $apiInstance->deleteApiTickets($ids);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->deleteApiTickets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **string**| ticket ids to be deleted | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getApiTickets**
> object getApiTickets($new, $unassigned, $mine, $starred, $trashed, $label, $status, $agent, $customer, $priority, $group, $team, $tags, $mailbox, $sort, $page, $search, $act_as_type, $act_as_email)

Return a Collection of Tickets

Return a Collection of Tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$new = "new_example"; // string | 
$unassigned = "unassigned_example"; // string | 
$mine = "mine_example"; // string | 
$starred = "starred_example"; // string | 
$trashed = "trashed_example"; // string | 
$label = "label_example"; // string | labelId
$status = "status_example"; // string | statusId
$agent = "agent_example"; // string | agentId
$customer = "customer_example"; // string | customerId
$priority = "priority_example"; // string | priorityId
$group = "group_example"; // string | groupId
$team = "team_example"; // string | teamId
$tags = "tags_example"; // string | tagId
$mailbox = "mailbox_example"; // string | mailboxId
$sort = "sort_example"; // string | 
$page = "page_example"; // string | 
$search = "search_example"; // string | search for Ticket
$act_as_type = "act_as_type_example"; // string | admin can actAs customer, options: customer, agent
$act_as_email = "act_as_email_example"; // string | email of acted user

try {
    $result = $apiInstance->getApiTickets($new, $unassigned, $mine, $starred, $trashed, $label, $status, $agent, $customer, $priority, $group, $team, $tags, $mailbox, $sort, $page, $search, $act_as_type, $act_as_email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->getApiTickets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **new** | **string**|  | [optional]
 **unassigned** | **string**|  | [optional]
 **mine** | **string**|  | [optional]
 **starred** | **string**|  | [optional]
 **trashed** | **string**|  | [optional]
 **label** | **string**| labelId | [optional]
 **status** | **string**| statusId | [optional]
 **agent** | **string**| agentId | [optional]
 **customer** | **string**| customerId | [optional]
 **priority** | **string**| priorityId | [optional]
 **group** | **string**| groupId | [optional]
 **team** | **string**| teamId | [optional]
 **tags** | **string**| tagId | [optional]
 **mailbox** | **string**| mailboxId | [optional]
 **sort** | **string**|  | [optional]
 **page** | **string**|  | [optional]
 **search** | **string**| search for Ticket | [optional]
 **act_as_type** | **string**| admin can actAs customer, options: customer, agent | [optional]
 **act_as_email** | **string**| email of acted user | [optional]

### Return type

**object**

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiTicketTags**
> postApiTicketTags($id, $name)

Add Tag from Ticket

Add Tag from Ticket

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$name = "name_example"; // string | tagname required for POST

try {
    $apiInstance->postApiTicketTags($id, $name);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->postApiTicketTags: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **name** | **string**| tagname required for POST | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postApiTickets**
> postApiTickets($type, $name, $from, $reply, $subject, $custom_fields, $act_as_type, $act_as_email)

Add ticket

Add ticket

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$type = "type_example"; // string | 1|2|3|4|5|6 for open|pending|resolved|closed|Spam|Answered repectively
$name = "name_example"; // string | ticket name
$from = "from_example"; // string | email address
$reply = "reply_example"; // string | reply content
$subject = "subject_example"; // string | ticket subject
$custom_fields = "custom_fields_example"; // string | custom fields (if present) could be provided
$act_as_type = "act_as_type_example"; // string | admin can actAsType customer, agent
$act_as_email = "act_as_email_example"; // string | provide when acting as agent

try {
    $apiInstance->postApiTickets($type, $name, $from, $reply, $subject, $custom_fields, $act_as_type, $act_as_email);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->postApiTickets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **string**| 1|2|3|4|5|6 for open|pending|resolved|closed|Spam|Answered repectively | [optional]
 **name** | **string**| ticket name | [optional]
 **from** | **string**| email address | [optional]
 **reply** | **string**| reply content | [optional]
 **subject** | **string**| ticket subject | [optional]
 **custom_fields** | **string**| custom fields (if present) could be provided | [optional]
 **act_as_type** | **string**| admin can actAsType customer, agent | [optional]
 **act_as_email** | **string**| provide when acting as agent | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicketsAgent**
> putApiTicketsAgent($ids, $agent_id)

Assign Agent to multiple Tickets

Assign Agent to multiple Tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ids = "ids_example"; // string | ticket ids
$agent_id = "agent_id_example"; // string | agent id

try {
    $apiInstance->putApiTicketsAgent($ids, $agent_id);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->putApiTicketsAgent: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **string**| ticket ids | [optional]
 **agent_id** | **string**| agent id | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicketsGroup**
> putApiTicketsGroup($ids, $group_id)

change Group of multiple Tickets

change Group of multiple Tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ids = "ids_example"; // string | ticket ids
$group_id = "group_id_example"; // string | group id

try {
    $apiInstance->putApiTicketsGroup($ids, $group_id);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->putApiTicketsGroup: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **string**| ticket ids | [optional]
 **group_id** | **string**| group id | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicketsLabel**
> putApiTicketsLabel($ids, $label_id)

add label to multiple Tickets

add label to multiple Tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ids = "ids_example"; // string | ticket ids
$label_id = "label_id_example"; // string | label id

try {
    $apiInstance->putApiTicketsLabel($ids, $label_id);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->putApiTicketsLabel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **string**| ticket ids | [optional]
 **label_id** | **string**| label id | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicketsPriority**
> putApiTicketsPriority($ids, $priority_id)

change Priority of multiple Tickets

change Priority of multiple Tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ids = "ids_example"; // string | ticket ids
$priority_id = "priority_id_example"; // string | priority id

try {
    $apiInstance->putApiTicketsPriority($ids, $priority_id);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->putApiTicketsPriority: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **string**| ticket ids | [optional]
 **priority_id** | **string**| priority id | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicketsRestore**
> putApiTicketsRestore($ids)

Restore multiple Tickets

Restore multiple Tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ids = "ids_example"; // string | ticket ids to be restored

try {
    $apiInstance->putApiTicketsRestore($ids);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->putApiTicketsRestore: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **string**| ticket ids to be restored | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicketsStatus**
> putApiTicketsStatus($ids, $status_id)

change Status of multiple Tickets

change Status of multiple Tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ids = "ids_example"; // string | ticket ids
$status_id = "status_id_example"; // string | status id

try {
    $apiInstance->putApiTicketsStatus($ids, $status_id);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->putApiTicketsStatus: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **string**| ticket ids | [optional]
 **status_id** | **string**| status id | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putApiTicketsTrash**
> putApiTicketsTrash($ids)

Trash multiple Tickets

Trash multiple Tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: password
$config = UvdeskApi\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new UvdeskApi\Api\TicketsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ids = "ids_example"; // string | ticket ids to be trashed

try {
    $apiInstance->putApiTicketsTrash($ids);
} catch (Exception $e) {
    echo 'Exception when calling TicketsApi->putApiTicketsTrash: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **string**| ticket ids to be trashed | [optional]

### Return type

void (empty response body)

### Authorization

[password](../../README.md#password)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

