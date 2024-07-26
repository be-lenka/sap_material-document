# BeLenka\SAP\MaterialDocument\SerialNumbersApi

All URIs are relative to https://:/sap/opu/odata/sap/API_MATERIAL_DOCUMENT_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet()**](SerialNumbersApi.md#aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;)/to_SerialNumbers | Reads information on serial numbers for a specific material document item |
| [**aSerialNumberMaterialDocumentGet()**](SerialNumbersApi.md#aSerialNumberMaterialDocumentGet) | **GET** /A_SerialNumberMaterialDocument | Reads information of serial numbers on material document items level |
| [**aSerialNumberMaterialDocumentMaterialMaterialSerialNumberSerialNumberMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearGet()**](SerialNumbersApi.md#aSerialNumberMaterialDocumentMaterialMaterialSerialNumberSerialNumberMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearGet) | **GET** /A_SerialNumberMaterialDocument(Material&#x3D;&#39;{Material}&#39;,SerialNumber&#x3D;&#39;{SerialNumber}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;,MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;) | Reads information of serial number on material document item level for a specific material document, item, year and material |


## `aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet()`

```php
aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet($material_document_year, $material_document, $material_document_item, $top, $skip, $filter, $inlinecount, $orderby, $select): \BeLenka\SAP\MaterialDocument\Model\Wrapper2
```

Reads information on serial numbers for a specific material document item

Reads information on serial numbers for a specific material document item to get an overview of the posted serial numbers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialDocument\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialDocument\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\SerialNumbersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material_document_year = 'material_document_year_example'; // string | Material Document Year
$material_document = 'material_document_example'; // string | Number of Material Document
$material_document_item = 'material_document_item_example'; // string | Material Document Item
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)

try {
    $result = $apiInstance->aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet($material_document_year, $material_document, $material_document_item, $top, $skip, $filter, $inlinecount, $orderby, $select);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SerialNumbersApi->aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material_document_year** | **string**| Material Document Year | |
| **material_document** | **string**| Number of Material Document | |
| **material_document_item** | **string**| Material Document Item | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialDocument\Model\Wrapper2**](../Model/Wrapper2.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aSerialNumberMaterialDocumentGet()`

```php
aSerialNumberMaterialDocumentGet($top, $skip, $filter, $inlinecount, $orderby, $select): \BeLenka\SAP\MaterialDocument\Model\Wrapper2
```

Reads information of serial numbers on material document items level

Reads information of serial numbers of material document items to get an overview of the posted serial numbers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialDocument\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialDocument\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\SerialNumbersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)

try {
    $result = $apiInstance->aSerialNumberMaterialDocumentGet($top, $skip, $filter, $inlinecount, $orderby, $select);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SerialNumbersApi->aSerialNumberMaterialDocumentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialDocument\Model\Wrapper2**](../Model/Wrapper2.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aSerialNumberMaterialDocumentMaterialMaterialSerialNumberSerialNumberMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearGet()`

```php
aSerialNumberMaterialDocumentMaterialMaterialSerialNumberSerialNumberMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearGet($material, $serial_number, $material_document, $material_document_item, $material_document_year, $select): \BeLenka\SAP\MaterialDocument\Model\ASerialNumberMaterialDocumentType
```

Reads information of serial number on material document item level for a specific material document, item, year and material

Reads information of serial number of a specific material document, item, year and material to get an overview of the posted serial numbers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialDocument\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialDocument\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\SerialNumbersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material = 'material_example'; // string | Material Number
$serial_number = 'serial_number_example'; // string | Serial Number
$material_document = 'material_document_example'; // string | Number of Material Document
$material_document_item = 'material_document_item_example'; // string | Material Document Item
$material_document_year = 'material_document_year_example'; // string | Material Document Year
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)

try {
    $result = $apiInstance->aSerialNumberMaterialDocumentMaterialMaterialSerialNumberSerialNumberMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearGet($material, $serial_number, $material_document, $material_document_item, $material_document_year, $select);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SerialNumbersApi->aSerialNumberMaterialDocumentMaterialMaterialSerialNumberSerialNumberMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material** | **string**| Material Number | |
| **serial_number** | **string**| Serial Number | |
| **material_document** | **string**| Number of Material Document | |
| **material_document_item** | **string**| Material Document Item | |
| **material_document_year** | **string**| Material Document Year | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialDocument\Model\ASerialNumberMaterialDocumentType**](../Model/ASerialNumberMaterialDocumentType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
