# OpenAPIClient-php

This service enables you to retrieve and create material documents, for example, to post a goods receipt for a purchase order or to document the transfer of materials between two storage locations. Additionally, the service allows you to cancel existing material documents or single items. It can be consumed by external systems and user interfaces.


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialDocument\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialDocument\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\BatchRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->batchPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchRequestsApi->batchPost: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://:/sap/opu/odata/sap/API_MATERIAL_DOCUMENT_SRV*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BatchRequestsApi* | [**batchPost**](docs/Api/BatchRequestsApi.md#batchpost) | **POST** /$batch | Send a group of requests
*DocumentHeaderApi* | [**aMaterialDocumentHeaderGet**](docs/Api/DocumentHeaderApi.md#amaterialdocumentheaderget) | **GET** /A_MaterialDocumentHeader | Reads information on material document header level
*DocumentHeaderApi* | [**aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentGet**](docs/Api/DocumentHeaderApi.md#amaterialdocumentheadermaterialdocumentyearmaterialdocumentyearmaterialdocumentmaterialdocumentget) | **GET** /A_MaterialDocumentHeader(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;) | Reads information for a specific material document header
*DocumentHeaderApi* | [**aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet**](docs/Api/DocumentHeaderApi.md#amaterialdocumentheadermaterialdocumentyearmaterialdocumentyearmaterialdocumentmaterialdocumenttomaterialdocumentitemget) | **GET** /A_MaterialDocumentHeader(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;)/to_MaterialDocumentItem | Reads information for a specific material document header and material document items
*DocumentHeaderApi* | [**aMaterialDocumentHeaderPost**](docs/Api/DocumentHeaderApi.md#amaterialdocumentheaderpost) | **POST** /A_MaterialDocumentHeader | Creates a material document
*DocumentHeaderApi* | [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet**](docs/Api/DocumentHeaderApi.md#amaterialdocumentitemmaterialdocumentyearmaterialdocumentyearmaterialdocumentmaterialdocumentmaterialdocumentitemmaterialdocumentitemtomaterialdocumentheaderget) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;)/to_MaterialDocumentHeader | Reads information on material document item and header level for a specific material document item
*DocumentHeaderApi* | [**cancelPost**](docs/Api/DocumentHeaderApi.md#cancelpost) | **POST** /Cancel | Cancels a material document
*DocumentItemsApi* | [**aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet**](docs/Api/DocumentItemsApi.md#amaterialdocumentheadermaterialdocumentyearmaterialdocumentyearmaterialdocumentmaterialdocumenttomaterialdocumentitemget) | **GET** /A_MaterialDocumentHeader(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;)/to_MaterialDocumentItem | Reads information for a specific material document header and material document items
*DocumentItemsApi* | [**aMaterialDocumentItemGet**](docs/Api/DocumentItemsApi.md#amaterialdocumentitemget) | **GET** /A_MaterialDocumentItem | Reads information on material document items level
*DocumentItemsApi* | [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemGet**](docs/Api/DocumentItemsApi.md#amaterialdocumentitemmaterialdocumentyearmaterialdocumentyearmaterialdocumentmaterialdocumentmaterialdocumentitemmaterialdocumentitemget) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;) | Reads information on material document items level for a specific material document
*DocumentItemsApi* | [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet**](docs/Api/DocumentItemsApi.md#amaterialdocumentitemmaterialdocumentyearmaterialdocumentyearmaterialdocumentmaterialdocumentmaterialdocumentitemmaterialdocumentitemtomaterialdocumentheaderget) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;)/to_MaterialDocumentHeader | Reads information on material document item and header level for a specific material document item
*DocumentItemsApi* | [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet**](docs/Api/DocumentItemsApi.md#amaterialdocumentitemmaterialdocumentyearmaterialdocumentyearmaterialdocumentmaterialdocumentmaterialdocumentitemmaterialdocumentitemtoserialnumbersget) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;)/to_SerialNumbers | Reads information on serial numbers for a specific material document item
*DocumentItemsApi* | [**cancelItemPost**](docs/Api/DocumentItemsApi.md#cancelitempost) | **POST** /CancelItem | Cancels a material document item
*SerialNumbersApi* | [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet**](docs/Api/SerialNumbersApi.md#amaterialdocumentitemmaterialdocumentyearmaterialdocumentyearmaterialdocumentmaterialdocumentmaterialdocumentitemmaterialdocumentitemtoserialnumbersget) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;)/to_SerialNumbers | Reads information on serial numbers for a specific material document item
*SerialNumbersApi* | [**aSerialNumberMaterialDocumentGet**](docs/Api/SerialNumbersApi.md#aserialnumbermaterialdocumentget) | **GET** /A_SerialNumberMaterialDocument | Reads information of serial numbers on material document items level
*SerialNumbersApi* | [**aSerialNumberMaterialDocumentMaterialMaterialSerialNumberSerialNumberMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearGet**](docs/Api/SerialNumbersApi.md#aserialnumbermaterialdocumentmaterialmaterialserialnumberserialnumbermaterialdocumentmaterialdocumentmaterialdocumentitemmaterialdocumentitemmaterialdocumentyearmaterialdocumentyearget) | **GET** /A_SerialNumberMaterialDocument(Material&#x3D;&#39;{Material}&#39;,SerialNumber&#x3D;&#39;{SerialNumber}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;,MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;) | Reads information of serial number on material document item level for a specific material document, item, year and material

## Models

- [AMaterialDocumentHeaderType](docs/Model/AMaterialDocumentHeaderType.md)
- [AMaterialDocumentItemType](docs/Model/AMaterialDocumentItemType.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderType](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderType.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreate](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreate.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreateToMaterialDocumentItem](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreateToMaterialDocumentItem.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeToMaterialDocumentItem](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeToMaterialDocumentItem.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeUpdate](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeUpdate.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentItemType](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentItemType.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeCreate](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeCreate.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeCreateToSerialNumbers](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeCreateToSerialNumbers.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeToSerialNumbers](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeToSerialNumbers.md)
- [APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeUpdate](docs/Model/APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeUpdate.md)
- [APIMATERIALDOCUMENTSRVASerialNumberMaterialDocumentType](docs/Model/APIMATERIALDOCUMENTSRVASerialNumberMaterialDocumentType.md)
- [APIMATERIALDOCUMENTSRVASerialNumberMaterialDocumentTypeCreate](docs/Model/APIMATERIALDOCUMENTSRVASerialNumberMaterialDocumentTypeCreate.md)
- [APIMATERIALDOCUMENTSRVASerialNumberMaterialDocumentTypeUpdate](docs/Model/APIMATERIALDOCUMENTSRVASerialNumberMaterialDocumentTypeUpdate.md)
- [ASerialNumberMaterialDocumentType](docs/Model/ASerialNumberMaterialDocumentType.md)
- [CollectionOfAMaterialDocumentHeaderType](docs/Model/CollectionOfAMaterialDocumentHeaderType.md)
- [CollectionOfAMaterialDocumentItemType](docs/Model/CollectionOfAMaterialDocumentItemType.md)
- [CollectionOfASerialNumberMaterialDocumentType](docs/Model/CollectionOfASerialNumberMaterialDocumentType.md)
- [Error](docs/Model/Error.md)
- [ErrorError](docs/Model/ErrorError.md)
- [ErrorErrorMessage](docs/Model/ErrorErrorMessage.md)
- [Wrapper](docs/Model/Wrapper.md)
- [Wrapper1](docs/Model/Wrapper1.md)
- [Wrapper2](docs/Model/Wrapper2.md)

## Authorization

Authentication schemes defined for the API:
### OAuth2Auth

- **Type**: `OAuth`
- **Flow**: `accessCode`
- **Authorization URL**: `https://{host}:{port}`
- **Scopes**: 
    - **API_MATERIAL_DOCUMENT_SRV_0001**: 

### BasicAuth

- **Type**: HTTP basic authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.3.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
