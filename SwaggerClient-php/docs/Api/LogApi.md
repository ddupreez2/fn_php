# Swagger\Client\LogApi

All URIs are relative to *https://127.0.0.1:8080/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**appsAppCallsCallLogDelete**](LogApi.md#appsAppCallsCallLogDelete) | **DELETE** /apps/{app}/calls/{call}/log | Delete call log entry
[**appsAppCallsCallLogGet**](LogApi.md#appsAppCallsCallLogGet) | **GET** /apps/{app}/calls/{call}/log | Get call logs


# **appsAppCallsCallLogDelete**
> appsAppCallsCallLogDelete($call, $app)

Delete call log entry

Delete call log entry

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\LogApi();
$call = "call_example"; // string | Call ID.
$app = "app_example"; // string | App name.

try {
    $api_instance->appsAppCallsCallLogDelete($call, $app);
} catch (Exception $e) {
    echo 'Exception when calling LogApi->appsAppCallsCallLogDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **call** | **string**| Call ID. |
 **app** | **string**| App name. |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **appsAppCallsCallLogGet**
> \Swagger\Client\Model\LogWrapper appsAppCallsCallLogGet($app, $call)

Get call logs

Get call logs

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\LogApi();
$app = "app_example"; // string | App Name
$call = "call_example"; // string | Call ID.

try {
    $result = $api_instance->appsAppCallsCallLogGet($app, $call);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LogApi->appsAppCallsCallLogGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | **string**| App Name |
 **call** | **string**| Call ID. |

### Return type

[**\Swagger\Client\Model\LogWrapper**](../Model/LogWrapper.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

