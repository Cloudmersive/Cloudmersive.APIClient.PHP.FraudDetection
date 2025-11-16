# Swagger\Client\FraudDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**documentDetectFraud**](FraudDetectionApi.md#documentDetectFraud) | **POST** /fraud-ai/detection/document | AI Fraud Detection for Documents
[**documentDetectFraudAdvanced**](FraudDetectionApi.md#documentDetectFraudAdvanced) | **POST** /fraud-ai/detection/document/advanced | Advanced AI Fraud Detection for Documents


# **documentDetectFraud**
> \Swagger\Client\Model\FraudDetectionResult documentDetectFraud($input_file)

AI Fraud Detection for Documents

Perform fraud detection and classification on input document and user context.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\FraudDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input document, or photos of a document, to perform fraud detection on

try {
    $result = $apiInstance->documentDetectFraud($input_file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FraudDetectionApi->documentDetectFraud: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input document, or photos of a document, to perform fraud detection on | [optional]

### Return type

[**\Swagger\Client\Model\FraudDetectionResult**](../Model/FraudDetectionResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **documentDetectFraudAdvanced**
> \Swagger\Client\Model\AdvancedFraudDetectionResult documentDetectFraudAdvanced($user_email_address, $user_email_address_verified, $input_file)

Advanced AI Fraud Detection for Documents

Perform advanced fraud detection and classification on input document and user context.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\FraudDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_email_address = "user_email_address_example"; // string | User email address for context (optional)
$user_email_address_verified = true; // bool | True if the user's email address was verified (optional)
$input_file = "/path/to/file.txt"; // \SplFileObject | Input document, or photos of a document, to perform fraud detection on

try {
    $result = $apiInstance->documentDetectFraudAdvanced($user_email_address, $user_email_address_verified, $input_file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FraudDetectionApi->documentDetectFraudAdvanced: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_email_address** | **string**| User email address for context (optional) | [optional]
 **user_email_address_verified** | **bool**| True if the user&#39;s email address was verified (optional) | [optional]
 **input_file** | **\SplFileObject**| Input document, or photos of a document, to perform fraud detection on | [optional]

### Return type

[**\Swagger\Client\Model\AdvancedFraudDetectionResult**](../Model/AdvancedFraudDetectionResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

