# Swagger\Client\RoutesApi

All URIs are relative to *https://127.0.0.1:8080/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**appsAppRoutesGet**](RoutesApi.md#appsAppRoutesGet) | **GET** /apps/{app}/routes | Get route list by app name.
[**appsAppRoutesPost**](RoutesApi.md#appsAppRoutesPost) | **POST** /apps/{app}/routes | Create new Route
[**appsAppRoutesRouteDelete**](RoutesApi.md#appsAppRoutesRouteDelete) | **DELETE** /apps/{app}/routes/{route} | Deletes the route
[**appsAppRoutesRouteGet**](RoutesApi.md#appsAppRoutesRouteGet) | **GET** /apps/{app}/routes/{route} | Gets route by name
[**appsAppRoutesRoutePatch**](RoutesApi.md#appsAppRoutesRoutePatch) | **PATCH** /apps/{app}/routes/{route} | Update a Route, Fails if the route or app does not exist. Accepts partial updates / skips validation of zero values.
[**appsAppRoutesRoutePut**](RoutesApi.md#appsAppRoutesRoutePut) | **PUT** /apps/{app}/routes/{route} | Create a Route if it does not exist. Update if it does. Will also create app if it does not exist. Put does not skip validation of zero values


# **appsAppRoutesGet**
> \Swagger\Client\Model\RoutesWrapper appsAppRoutesGet($app, $image, $cursor, $per_page)

Get route list by app name.

This will list routes for a particular app, returned in alphabetical order.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\RoutesApi();
$app = "app_example"; // string | Name of app for this set of routes.
$image = "image_example"; // string | Route image to match, exact.
$cursor = "cursor_example"; // string | Cursor from previous response.next_cursor to begin results after, if any.
$per_page = 56; // int | Number of results to return, defaults to 30. Max of 100.

try {
    $result = $api_instance->appsAppRoutesGet($app, $image, $cursor, $per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoutesApi->appsAppRoutesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | **string**| Name of app for this set of routes. |
 **image** | **string**| Route image to match, exact. | [optional]
 **cursor** | **string**| Cursor from previous response.next_cursor to begin results after, if any. | [optional]
 **per_page** | **int**| Number of results to return, defaults to 30. Max of 100. | [optional]

### Return type

[**\Swagger\Client\Model\RoutesWrapper**](../Model/RoutesWrapper.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **appsAppRoutesPost**
> \Swagger\Client\Model\RouteWrapper appsAppRoutesPost($app, $body)

Create new Route

Create a new route in an app, if app doesn't exists, it creates the app. Post does not skip validation of zero values.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\RoutesApi();
$app = "app_example"; // string | name of the app.
$body = new \Swagger\Client\Model\RouteWrapper(); // \Swagger\Client\Model\RouteWrapper | One route to post.

try {
    $result = $api_instance->appsAppRoutesPost($app, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoutesApi->appsAppRoutesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | **string**| name of the app. |
 **body** | [**\Swagger\Client\Model\RouteWrapper**](../Model/RouteWrapper.md)| One route to post. |

### Return type

[**\Swagger\Client\Model\RouteWrapper**](../Model/RouteWrapper.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **appsAppRoutesRouteDelete**
> appsAppRoutesRouteDelete($app, $route)

Deletes the route

Deletes the route.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\RoutesApi();
$app = "app_example"; // string | Name of app for this set of routes.
$route = "route_example"; // string | Route name

try {
    $api_instance->appsAppRoutesRouteDelete($app, $route);
} catch (Exception $e) {
    echo 'Exception when calling RoutesApi->appsAppRoutesRouteDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | **string**| Name of app for this set of routes. |
 **route** | **string**| Route name |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **appsAppRoutesRouteGet**
> \Swagger\Client\Model\RouteWrapper appsAppRoutesRouteGet($app, $route)

Gets route by name

Gets a route by name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\RoutesApi();
$app = "app_example"; // string | Name of app for this set of routes.
$route = "route_example"; // string | Route name

try {
    $result = $api_instance->appsAppRoutesRouteGet($app, $route);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoutesApi->appsAppRoutesRouteGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | **string**| Name of app for this set of routes. |
 **route** | **string**| Route name |

### Return type

[**\Swagger\Client\Model\RouteWrapper**](../Model/RouteWrapper.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **appsAppRoutesRoutePatch**
> \Swagger\Client\Model\RouteWrapper appsAppRoutesRoutePatch($app, $route, $body)

Update a Route, Fails if the route or app does not exist. Accepts partial updates / skips validation of zero values.

Update a route

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\RoutesApi();
$app = "app_example"; // string | name of the app.
$route = "route_example"; // string | route path.
$body = new \Swagger\Client\Model\RouteWrapper(); // \Swagger\Client\Model\RouteWrapper | One route to post.

try {
    $result = $api_instance->appsAppRoutesRoutePatch($app, $route, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoutesApi->appsAppRoutesRoutePatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | **string**| name of the app. |
 **route** | **string**| route path. |
 **body** | [**\Swagger\Client\Model\RouteWrapper**](../Model/RouteWrapper.md)| One route to post. |

### Return type

[**\Swagger\Client\Model\RouteWrapper**](../Model/RouteWrapper.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **appsAppRoutesRoutePut**
> \Swagger\Client\Model\RouteWrapper appsAppRoutesRoutePut($app, $route, $body)

Create a Route if it does not exist. Update if it does. Will also create app if it does not exist. Put does not skip validation of zero values

Update or Create a route

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\RoutesApi();
$app = "app_example"; // string | name of the app.
$route = "route_example"; // string | route path.
$body = new \Swagger\Client\Model\RouteWrapper(); // \Swagger\Client\Model\RouteWrapper | One route to post.

try {
    $result = $api_instance->appsAppRoutesRoutePut($app, $route, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RoutesApi->appsAppRoutesRoutePut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | **string**| name of the app. |
 **route** | **string**| route path. |
 **body** | [**\Swagger\Client\Model\RouteWrapper**](../Model/RouteWrapper.md)| One route to post. |

### Return type

[**\Swagger\Client\Model\RouteWrapper**](../Model/RouteWrapper.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

