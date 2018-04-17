# WsApiClient\SearchApi

All URIs are relative to *https://api.wheel-size.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**searchByHfTireList**](SearchApi.md#searchByHfTireList) | **GET** /search/by_hf_tire/ | Find models matching given high flotation tire
[**searchByModelList**](SearchApi.md#searchByModelList) | **GET** /search/by_model/ | Find OE and option fitments by model/year/trim
[**searchByRimList**](SearchApi.md#searchByRimList) | **GET** /search/by_rim/ | Find models matching given rim parameters
[**searchByTireList**](SearchApi.md#searchByTireList) | **GET** /search/by_tire/ | Find models matching given tire parameters


# **searchByHfTireList**
> \WsApiClient\Model\MakeWithModels[] searchByHfTireList($tire_diameter, $tire_section_width, $rim_diameter_hf, $lang, $brands, $brands_exclude, $countries, $countries_exclude)

Find models matching given high flotation tire

Get a list of model modifications that match the given tire size in high flotation sizing system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: user_key
$config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKey('user_key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('user_key', 'Bearer');

$apiInstance = new WsApiClient\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tire_diameter = 31; // float | Tire diameter, in (e.g. `31`)
$tire_section_width = 10.5; // float | Tire section width, in (e.g. `10.5`)
$rim_diameter_hf = 15; // float | Rim diameter, in (e.g. `15`)
$lang = "lang_example"; // string | Use this parameter anywhere in the API to get *`name`* field translation of the following objects: **`Make`**, **`Model`**, **`Market`**. Across the *`name`* this objects will have *`name_en`* field with original english name. By default `en` language is used.  Available languages: `en,de,ru,es,pt,fr,ja,zh-cn`. Currently translation works for chinese `zh-cn` language only
$brands = "brands_example"; // string | Show information only for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `mitsubishi,nissan,toyota`)
$brands_exclude = "brands_exclude_example"; // string | Don't show information for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `geely,great-wall`)
$countries = "countries_example"; // string | Show information for local manufacturers from specified countries only. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `us,gb,jp`)
$countries_exclude = "countries_exclude_example"; // string | Don't show information for local manufacturers from specified countries. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `ru,ua`)

try {
    $result = $apiInstance->searchByHfTireList($tire_diameter, $tire_section_width, $rim_diameter_hf, $lang, $brands, $brands_exclude, $countries, $countries_exclude);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchByHfTireList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tire_diameter** | **float**| Tire diameter, in (e.g. &#x60;31&#x60;) |
 **tire_section_width** | **float**| Tire section width, in (e.g. &#x60;10.5&#x60;) |
 **rim_diameter_hf** | **float**| Rim diameter, in (e.g. &#x60;15&#x60;) |
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

# **searchByModelList**
> \WsApiClient\Model\Vehicle[] searchByModelList($make, $model, $year, $trim, $only_oem, $lang)

Find OE and option fitments by model/year/trim

Find OE and option fitments that match the given manufacturer, model, year and trim.  **It's an alias** for _**`GET /vehicles/`**_ method

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: user_key
$config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKey('user_key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('user_key', 'Bearer');

$apiInstance = new WsApiClient\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$make = "\"mitsubishi\""; // string | Manufacturer slug name, use _**`GET /makes/`**_ to get possible values (e.g. `mitsubishi`)
$model = "\"outlander\""; // string | Model slug name, use _**`GET /models/`**_ to get possible values (e.g. `outlander`)
$year = 2015; // int | You can use _**`GET /years/`**_ to get possible years (e.g. `2015`)
$trim = "trim_example"; // string | Use *`slug`* from _**`GET /trims/`**_ methods here. (e.g. `2.0+GG2W`)
$only_oem = true; // bool | Show only original equipment wheels
$lang = "lang_example"; // string | Use this parameter anywhere in the API to get *`name`* field translation of the following objects: **`Make`**, **`Model`**, **`Market`**. Across the *`name`* this objects will have *`name_en`* field with original english name. By default `en` language is used.  Available languages: `en,de,ru,es,pt,fr,ja,zh-cn`. Currently translation works for chinese `zh-cn` language only

try {
    $result = $apiInstance->searchByModelList($make, $model, $year, $trim, $only_oem, $lang);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchByModelList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **make** | **string**| Manufacturer slug name, use _**&#x60;GET /makes/&#x60;**_ to get possible values (e.g. &#x60;mitsubishi&#x60;) |
 **model** | **string**| Model slug name, use _**&#x60;GET /models/&#x60;**_ to get possible values (e.g. &#x60;outlander&#x60;) |
 **year** | **int**| You can use _**&#x60;GET /years/&#x60;**_ to get possible years (e.g. &#x60;2015&#x60;) |
 **trim** | **string**| Use *&#x60;slug&#x60;* from _**&#x60;GET /trims/&#x60;**_ methods here. (e.g. &#x60;2.0+GG2W&#x60;) | [optional]
 **only_oem** | **bool**| Show only original equipment wheels | [optional]
 **lang** | **string**| Use this parameter anywhere in the API to get *&#x60;name&#x60;* field translation of the following objects: **&#x60;Make&#x60;**, **&#x60;Model&#x60;**, **&#x60;Market&#x60;**. Across the *&#x60;name&#x60;* this objects will have *&#x60;name_en&#x60;* field with original english name. By default &#x60;en&#x60; language is used.  Available languages: &#x60;en,de,ru,es,pt,fr,ja,zh-cn&#x60;. Currently translation works for chinese &#x60;zh-cn&#x60; language only | [optional]

### Return type

[**\WsApiClient\Model\Vehicle[]**](../Model/Vehicle.md)

### Authorization

[user_key](../../README.md#user_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **searchByRimList**
> \WsApiClient\Model\MakeWithModels[] searchByRimList($bolt_pattern, $rim_diameter, $rim_width, $offset, $offset_min, $offset_max, $cb, $cb_min, $cb_max, $lang, $brands, $brands_exclude, $countries, $countries_exclude)

Find models matching given rim parameters

Get a list of model modifications that match the given rim parameters, grouped by manufacturer.  It's an alias for _**`GET /bolt-patterns/{bolt_pattern}/`**_        method with given path and query parameters.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: user_key
$config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKey('user_key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('user_key', 'Bearer');

$apiInstance = new WsApiClient\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bolt_pattern = "\"5x105\""; // string | Bolt pattern combines number of stud holes and pitch circle diameter. Use _**`GET /bolt-patterns/`**_ to get possible values (e.g. `5x105`)
$rim_diameter = 16; // float | Rim diameter, in (e.g. `16`)
$rim_width = 7; // float | Rim width, in (e.g. `7`)
$offset = 8.14; // float | Rim offset, mm (e.g. `40`)
$offset_min = 8.14; // float | Lower bound for rim offset, mm (e.g. `35`)
$offset_max = 8.14; // float | Upper bound for rim offset, mm (e.g. `45`)
$cb = 8.14; // float | Centre bore value, mm (e.g. `60`)
$cb_min = 8.14; // float | Lower bound for centre bore value, mm (e.g. `55`)
$cb_max = 8.14; // float | Upper bound for centre bore value, mm (e.g. `65`)
$lang = "lang_example"; // string | Use this parameter anywhere in the API to get *`name`* field translation of the following objects: **`Make`**, **`Model`**, **`Market`**. Across the *`name`* this objects will have *`name_en`* field with original english name. By default `en` language is used.  Available languages: `en,de,ru,es,pt,fr,ja,zh-cn`. Currently translation works for chinese `zh-cn` language only
$brands = "brands_example"; // string | Show information only for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `mitsubishi,nissan,toyota`)
$brands_exclude = "brands_exclude_example"; // string | Don't show information for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `geely,great-wall`)
$countries = "countries_example"; // string | Show information for local manufacturers from specified countries only. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `us,gb,jp`)
$countries_exclude = "countries_exclude_example"; // string | Don't show information for local manufacturers from specified countries. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `ru,ua`)

try {
    $result = $apiInstance->searchByRimList($bolt_pattern, $rim_diameter, $rim_width, $offset, $offset_min, $offset_max, $cb, $cb_min, $cb_max, $lang, $brands, $brands_exclude, $countries, $countries_exclude);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchByRimList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bolt_pattern** | **string**| Bolt pattern combines number of stud holes and pitch circle diameter. Use _**&#x60;GET /bolt-patterns/&#x60;**_ to get possible values (e.g. &#x60;5x105&#x60;) |
 **rim_diameter** | **float**| Rim diameter, in (e.g. &#x60;16&#x60;) |
 **rim_width** | **float**| Rim width, in (e.g. &#x60;7&#x60;) |
 **offset** | **float**| Rim offset, mm (e.g. &#x60;40&#x60;) | [optional]
 **offset_min** | **float**| Lower bound for rim offset, mm (e.g. &#x60;35&#x60;) | [optional]
 **offset_max** | **float**| Upper bound for rim offset, mm (e.g. &#x60;45&#x60;) | [optional]
 **cb** | **float**| Centre bore value, mm (e.g. &#x60;60&#x60;) | [optional]
 **cb_min** | **float**| Lower bound for centre bore value, mm (e.g. &#x60;55&#x60;) | [optional]
 **cb_max** | **float**| Upper bound for centre bore value, mm (e.g. &#x60;65&#x60;) | [optional]
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

# **searchByTireList**
> \WsApiClient\Model\MakeWithModels[] searchByTireList($tire_width, $aspect_ratio, $rim_diameter, $lang, $brands, $brands_exclude, $countries, $countries_exclude)

Find models matching given tire parameters

Get a list of model modifications matching given tire, grouped by manufacturer.  It's an alias for _**`GET /tire/{tire}/`**_ method  (tire configuration is combined of required tire width, aspect ratio and rim diameter).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: user_key
$config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKey('user_key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('user_key', 'Bearer');

$apiInstance = new WsApiClient\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tire_width = 195; // float | Tire width, mm (e.g. `195`)
$aspect_ratio = 50; // float | Aspect ratio, % (e.g. `50`)
$rim_diameter = 16; // float | Rim diameter, in (e.g. `16`)
$lang = "lang_example"; // string | Use this parameter anywhere in the API to get *`name`* field translation of the following objects: **`Make`**, **`Model`**, **`Market`**. Across the *`name`* this objects will have *`name_en`* field with original english name. By default `en` language is used.  Available languages: `en,de,ru,es,pt,fr,ja,zh-cn`. Currently translation works for chinese `zh-cn` language only
$brands = "brands_example"; // string | Show information only for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `mitsubishi,nissan,toyota`)
$brands_exclude = "brands_exclude_example"; // string | Don't show information for specified manufacturers. Use _**`GET /makes/`**_ method to get the full list. (e.g. `geely,great-wall`)
$countries = "countries_example"; // string | Show information for local manufacturers from specified countries only. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `us,gb,jp`)
$countries_exclude = "countries_exclude_example"; // string | Don't show information for local manufacturers from specified countries. Use _**`GET /countries/`**_ method to get the full list of countries. (e.g. `ru,ua`)

try {
    $result = $apiInstance->searchByTireList($tire_width, $aspect_ratio, $rim_diameter, $lang, $brands, $brands_exclude, $countries, $countries_exclude);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchByTireList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tire_width** | **float**| Tire width, mm (e.g. &#x60;195&#x60;) |
 **aspect_ratio** | **float**| Aspect ratio, % (e.g. &#x60;50&#x60;) |
 **rim_diameter** | **float**| Rim diameter, in (e.g. &#x60;16&#x60;) |
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

