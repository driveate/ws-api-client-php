# WsApiClient\TiresApi

All URIs are relative to *https://api.wheel-size.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tiresList**](TiresApi.md#tiresList) | **GET** /tires/ | Returns a list of tires
[**tiresRead**](TiresApi.md#tiresRead) | **GET** /tires/{tire}/ | Model modifications matching given tire


# **tiresList**
> \WsApiClient\Model\Tire[] tiresList($width, $width_min, $width_max, $aspect_ratio, $aspect_ratio_min, $aspect_ratio_max, $rim_diameter, $rim_diameter_min, $rim_diameter_max, $brands, $brands_exclude, $countries, $countries_exclude)

Returns a list of tires

Get a list of tires with a number of matching model modifications

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: user_key
$config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKey('user_key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('user_key', 'Bearer');

$apiInstance = new WsApiClient\Api\TiresApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$width = 8.14; // float | Tire width, mm (e.g. `195`)
$width_min = 8.14; // float | Lower bound for tire width, mm (e.g. `165`)
$width_max = 8.14; // float | Upper bound for tire width, mm (e.g. `200`)
$aspect_ratio = 8.14; // float | Aspect ratio, % (e.g. `50`)
$aspect_ratio_min = 8.14; // float | Lower bound for aspect ratio, % (e.g. `30`)
$aspect_ratio_max = 8.14; // float | Upper bound for aspect ratio, % (e.g. `70`)
$rim_diameter = 8.14; // float | Rim diameter, in (e.g. `16`)
$rim_diameter_min = 8.14; // float | Lower bound for rim diameter, in (e.g. `13`)
$rim_diameter_max = 8.14; // float | Upper bound for rim diameter, in (e.g. `20`)
$brands = "brands_example"; // string | Show information only for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `mitsubishi,nissan,toyota`)
$brands_exclude = "brands_exclude_example"; // string | Don't show information for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `geely,great-wall`)
$countries = "countries_example"; // string | Show information for local manufacturers from specified countries only. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `us,gb,jp`)
$countries_exclude = "countries_exclude_example"; // string | Don't show information for local manufacturers from specified countries. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `ru,ua`)

try {
    $result = $apiInstance->tiresList($width, $width_min, $width_max, $aspect_ratio, $aspect_ratio_min, $aspect_ratio_max, $rim_diameter, $rim_diameter_min, $rim_diameter_max, $brands, $brands_exclude, $countries, $countries_exclude);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TiresApi->tiresList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **width** | **float**| Tire width, mm (e.g. &#x60;195&#x60;) | [optional]
 **width_min** | **float**| Lower bound for tire width, mm (e.g. &#x60;165&#x60;) | [optional]
 **width_max** | **float**| Upper bound for tire width, mm (e.g. &#x60;200&#x60;) | [optional]
 **aspect_ratio** | **float**| Aspect ratio, % (e.g. &#x60;50&#x60;) | [optional]
 **aspect_ratio_min** | **float**| Lower bound for aspect ratio, % (e.g. &#x60;30&#x60;) | [optional]
 **aspect_ratio_max** | **float**| Upper bound for aspect ratio, % (e.g. &#x60;70&#x60;) | [optional]
 **rim_diameter** | **float**| Rim diameter, in (e.g. &#x60;16&#x60;) | [optional]
 **rim_diameter_min** | **float**| Lower bound for rim diameter, in (e.g. &#x60;13&#x60;) | [optional]
 **rim_diameter_max** | **float**| Upper bound for rim diameter, in (e.g. &#x60;20&#x60;) | [optional]
 **brands** | **string**| Show information only for specified manufacturers. Use _**&#x60;GET /makes/&#x60;**_ method to get the full list. (e.g. &#x60;mitsubishi,nissan,toyota&#x60;) | [optional]
 **brands_exclude** | **string**| Don&#39;t show information for specified manufacturers. Use _**&#x60;GET /makes/&#x60;**_ method to get the full list. (e.g. &#x60;geely,great-wall&#x60;) | [optional]
 **countries** | **string**| Show information for local manufacturers from specified countries only. Use _**&#x60;GET /countries/&#x60;**_ method to get the full list of countries. (e.g. &#x60;us,gb,jp&#x60;) | [optional]
 **countries_exclude** | **string**| Don&#39;t show information for local manufacturers from specified countries. Use _**&#x60;GET /countries/&#x60;**_ method to get the full list of countries. (e.g. &#x60;ru,ua&#x60;) | [optional]

### Return type

[**\WsApiClient\Model\Tire[]**](../Model/Tire.md)

### Authorization

[user_key](../../README.md#user_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **tiresRead**
> \WsApiClient\Model\MakeWithModels[] tiresRead($tire, $width, $width_min, $width_max, $aspect_ratio, $aspect_ratio_min, $aspect_ratio_max, $rim_diameter, $rim_diameter_min, $rim_diameter_max, $lang, $brands, $brands_exclude, $countries, $countries_exclude)

Model modifications matching given tire

Get a list of model modifications by tire

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: user_key
$config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKey('user_key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('user_key', 'Bearer');

$apiInstance = new WsApiClient\Api\TiresApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tire = "\"195/50R15\""; // string | Formatted tire size. Use _**`GET /tires/`**_ to get possible values (e.g. `195/50R15`)
$width = 8.14; // float | Tire width, mm (e.g. `195`)
$width_min = 8.14; // float | Lower bound for tire width, mm (e.g. `165`)
$width_max = 8.14; // float | Upper bound for tire width, mm (e.g. `200`)
$aspect_ratio = 8.14; // float | Aspect ratio, % (e.g. `50`)
$aspect_ratio_min = 8.14; // float | Lower bound for aspect ratio, % (e.g. `30`)
$aspect_ratio_max = 8.14; // float | Upper bound for aspect ratio, % (e.g. `70`)
$rim_diameter = 8.14; // float | Rim diameter, in (e.g. `16`)
$rim_diameter_min = 8.14; // float | Lower bound for rim diameter, in (e.g. `13`)
$rim_diameter_max = 8.14; // float | Upper bound for rim diameter, in (e.g. `20`)
$lang = "lang_example"; // string | Use this parameter anywhere in the API to get *`name`* field translation of the following objects: **`Make`**, **`Model`**, **`Market`**. Across the *`name`* this objects will have *`name_en`* field with original english name. By default `en` language is used.  Available languages: `en,de,ru,es,pt,fr,ja,zh-cn`. Currently translation works for chinese `zh-cn` language only
$brands = "brands_example"; // string | Show information only for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `mitsubishi,nissan,toyota`)
$brands_exclude = "brands_exclude_example"; // string | Don't show information for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `geely,great-wall`)
$countries = "countries_example"; // string | Show information for local manufacturers from specified countries only. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `us,gb,jp`)
$countries_exclude = "countries_exclude_example"; // string | Don't show information for local manufacturers from specified countries. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `ru,ua`)

try {
    $result = $apiInstance->tiresRead($tire, $width, $width_min, $width_max, $aspect_ratio, $aspect_ratio_min, $aspect_ratio_max, $rim_diameter, $rim_diameter_min, $rim_diameter_max, $lang, $brands, $brands_exclude, $countries, $countries_exclude);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TiresApi->tiresRead: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tire** | **string**| Formatted tire size. Use _**&#x60;GET /tires/&#x60;**_ to get possible values (e.g. &#x60;195/50R15&#x60;) |
 **width** | **float**| Tire width, mm (e.g. &#x60;195&#x60;) | [optional]
 **width_min** | **float**| Lower bound for tire width, mm (e.g. &#x60;165&#x60;) | [optional]
 **width_max** | **float**| Upper bound for tire width, mm (e.g. &#x60;200&#x60;) | [optional]
 **aspect_ratio** | **float**| Aspect ratio, % (e.g. &#x60;50&#x60;) | [optional]
 **aspect_ratio_min** | **float**| Lower bound for aspect ratio, % (e.g. &#x60;30&#x60;) | [optional]
 **aspect_ratio_max** | **float**| Upper bound for aspect ratio, % (e.g. &#x60;70&#x60;) | [optional]
 **rim_diameter** | **float**| Rim diameter, in (e.g. &#x60;16&#x60;) | [optional]
 **rim_diameter_min** | **float**| Lower bound for rim diameter, in (e.g. &#x60;13&#x60;) | [optional]
 **rim_diameter_max** | **float**| Upper bound for rim diameter, in (e.g. &#x60;20&#x60;) | [optional]
 **lang** | **string**| Use this parameter anywhere in the API to get *&#x60;name&#x60;* field translation of the following objects: **&#x60;Make&#x60;**, **&#x60;Model&#x60;**, **&#x60;Market&#x60;**. Across the *&#x60;name&#x60;* this objects will have *&#x60;name_en&#x60;* field with original english name. By default &#x60;en&#x60; language is used.  Available languages: &#x60;en,de,ru,es,pt,fr,ja,zh-cn&#x60;. Currently translation works for chinese &#x60;zh-cn&#x60; language only | [optional]
 **brands** | **string**| Show information only for specified manufacturers. Use _**&#x60;GET /makes/&#x60;**_ method to get the full list. (e.g. &#x60;mitsubishi,nissan,toyota&#x60;) | [optional]
 **brands_exclude** | **string**| Don&#39;t show information for specified manufacturers. Use _**&#x60;GET /makes/&#x60;**_ method to get the full list. (e.g. &#x60;geely,great-wall&#x60;) | [optional]
 **countries** | **string**| Show information for local manufacturers from specified countries only. Use _**&#x60;GET /countries/&#x60;**_ method to get the full list of countries. (e.g. &#x60;us,gb,jp&#x60;) | [optional]
 **countries_exclude** | **string**| Don&#39;t show information for local manufacturers from specified countries. Use _**&#x60;GET /countries/&#x60;**_ method to get the full list of countries. (e.g. &#x60;ru,ua&#x60;) | [optional]

### Return type

[**\WsApiClient\Model\MakeWithModels[]**](../Model/MakeWithModels.md)

### Authorization

[user_key](../../README.md#user_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

