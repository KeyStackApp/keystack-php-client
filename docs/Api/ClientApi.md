# KeyStack\Client\ClientApi

All URIs are relative to http://localhost.

Method | HTTP request | Description
------------- | ------------- | -------------
[**activateLicense()**](ClientApi.md#activateLicense) | **POST** /v1/licenses/activate | 
[**deactivateLicense()**](ClientApi.md#deactivateLicense) | **POST** /v1/licenses/deactivate | 
[**manifestPublicRead()**](ClientApi.md#manifestPublicRead) | **GET** /v1/manifest/public-read/{cacheKey} | 
[**validateLicense()**](ClientApi.md#validateLicense) | **POST** /v1/licenses/validate | 


## `activateLicense()`

```php
activateLicense($activateLicense): \KeyStack\Client\Model\ActivationResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Client\Api\ClientApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$activateLicense = new \KeyStack\Client\Model\ActivateLicense(); // \KeyStack\Client\Model\ActivateLicense

try {
    $result = $apiInstance->activateLicense($activateLicense);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientApi->activateLicense: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **activateLicense** | [**\KeyStack\Client\Model\ActivateLicense**](../Model/ActivateLicense.md)|  | [optional]

### Return type

[**\KeyStack\Client\Model\ActivationResponse**](../Model/ActivationResponse.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deactivateLicense()`

```php
deactivateLicense($deactivateLicenseInput): \KeyStack\Client\Model\DeactivationResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Client\Api\ClientApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$deactivateLicenseInput = new \KeyStack\Client\Model\DeactivateLicenseInput(); // \KeyStack\Client\Model\DeactivateLicenseInput | The input parameters.

try {
    $result = $apiInstance->deactivateLicense($deactivateLicenseInput);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientApi->deactivateLicense: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deactivateLicenseInput** | [**\KeyStack\Client\Model\DeactivateLicenseInput**](../Model/DeactivateLicenseInput.md)| The input parameters. |

### Return type

[**\KeyStack\Client\Model\DeactivationResponse**](../Model/DeactivationResponse.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `manifestPublicRead()`

```php
manifestPublicRead($cacheKey): object
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new KeyStack\Client\Api\ClientApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client()
);
$cacheKey = test_manifest_key_1234; // string

try {
    $result = $apiInstance->manifestPublicRead($cacheKey);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientApi->manifestPublicRead: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cacheKey** | **string**|  |

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `validateLicense()`

```php
validateLicense($validateLicenseRequest): \KeyStack\Client\Model\LicenseKey
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Client\Api\ClientApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$validateLicenseRequest = new \KeyStack\Client\Model\ValidateLicenseRequest(); // \KeyStack\Client\Model\ValidateLicenseRequest

try {
    $result = $apiInstance->validateLicense($validateLicenseRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ClientApi->validateLicense: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **validateLicenseRequest** | [**\KeyStack\Client\Model\ValidateLicenseRequest**](../Model/ValidateLicenseRequest.md)|  | [optional]

### Return type

[**\KeyStack\Client\Model\LicenseKey**](../Model/LicenseKey.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
