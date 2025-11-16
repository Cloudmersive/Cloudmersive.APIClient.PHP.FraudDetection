# cloudmersive_fraud_detection_api_client
Easily and directly scan and block fraudulent security threats in input.

[Cloudmersive Fraud Detection API](https://cloudmersive.com/ai-fraud-detection-api) provides advanced AI fraud detection.

- API version: v1
- Package version: 3.0.0


## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/cloudmersive/cloudmersive_fraud_detection_api_client.git"
    }
  ],
  "require": {
    "cloudmersive/cloudmersive_fraud_detection_api_client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/cloudmersive_fraud_detection_api_client/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*FraudDetectionApi* | [**documentDetectFraud**](docs/Api/FraudDetectionApi.md#documentdetectfraud) | **POST** /fraud-ai/detection/document | AI Fraud Detection for Documents
*FraudDetectionApi* | [**documentDetectFraudAdvanced**](docs/Api/FraudDetectionApi.md#documentdetectfraudadvanced) | **POST** /fraud-ai/detection/document/advanced | Advanced AI Fraud Detection for Documents


## Documentation For Models

 - [AdvancedFraudDetectionResult](docs/Model/AdvancedFraudDetectionResult.md)
 - [FraudDetectionResult](docs/Model/FraudDetectionResult.md)


## Documentation For Authorization


## Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header


## Author




