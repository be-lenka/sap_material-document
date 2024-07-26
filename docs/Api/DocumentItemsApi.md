# BeLenka\SAP\MaterialDocument\DocumentItemsApi

All URIs are relative to https://:/sap/opu/odata/sap/API_MATERIAL_DOCUMENT_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet()**](DocumentItemsApi.md#aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet) | **GET** /A_MaterialDocumentHeader(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;)/to_MaterialDocumentItem | Reads information for a specific material document header and material document items |
| [**aMaterialDocumentItemGet()**](DocumentItemsApi.md#aMaterialDocumentItemGet) | **GET** /A_MaterialDocumentItem | Reads information on material document items level |
| [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemGet()**](DocumentItemsApi.md#aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemGet) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;) | Reads information on material document items level for a specific material document |
| [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet()**](DocumentItemsApi.md#aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;)/to_MaterialDocumentHeader | Reads information on material document item and header level for a specific material document item |
| [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet()**](DocumentItemsApi.md#aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;)/to_SerialNumbers | Reads information on serial numbers for a specific material document item |
| [**cancelItemPost()**](DocumentItemsApi.md#cancelItemPost) | **POST** /CancelItem | Cancels a material document item |


## `aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet()`

```php
aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet($material_document_year, $material_document, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\MaterialDocument\Model\Wrapper1
```

Reads information for a specific material document header and material document items

Reads material document header and material documents items information for a specific material document to get an overview of the material document posting.

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material_document_year = 'material_document_year_example'; // string | Material Document Year
$material_document = 'material_document_example'; // string | Number of Material Document
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet($material_document_year, $material_document, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentItemsApi->aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material_document_year** | **string**| Material Document Year | |
| **material_document** | **string**| Number of Material Document | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialDocument\Model\Wrapper1**](../Model/Wrapper1.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMaterialDocumentItemGet()`

```php
aMaterialDocumentItemGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\MaterialDocument\Model\Wrapper1
```

Reads information on material document items level

Reads material document items information to get an overview of the material document postings.

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentItemsApi(
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
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMaterialDocumentItemGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentItemsApi->aMaterialDocumentItemGet: ', $e->getMessage(), PHP_EOL;
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
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialDocument\Model\Wrapper1**](../Model/Wrapper1.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemGet()`

```php
aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemGet($material_document_year, $material_document, $material_document_item, $select, $expand): \BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentItemType
```

Reads information on material document items level for a specific material document

Reads material document items information for a specific material document and year to get an overview of the material document postings.

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material_document_year = 'material_document_year_example'; // string | Material Document Year
$material_document = 'material_document_example'; // string | Number of Material Document
$material_document_item = 'material_document_item_example'; // string | Material Document Item
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemGet($material_document_year, $material_document, $material_document_item, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentItemsApi->aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material_document_year** | **string**| Material Document Year | |
| **material_document** | **string**| Number of Material Document | |
| **material_document_item** | **string**| Material Document Item | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentItemType**](../Model/AMaterialDocumentItemType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet()`

```php
aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet($material_document_year, $material_document, $material_document_item, $select, $expand): \BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentHeaderType
```

Reads information on material document item and header level for a specific material document item

Reads material document item and header information for a specific material document, year and item to get an overview of the material document posting.

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material_document_year = 'material_document_year_example'; // string | Material Document Year
$material_document = 'material_document_example'; // string | Number of Material Document
$material_document_item = 'material_document_item_example'; // string | Material Document Item
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet($material_document_year, $material_document, $material_document_item, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentItemsApi->aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material_document_year** | **string**| Material Document Year | |
| **material_document** | **string**| Number of Material Document | |
| **material_document_item** | **string**| Material Document Item | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentHeaderType**](../Model/AMaterialDocumentHeaderType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentItemsApi(
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
    echo 'Exception when calling DocumentItemsApi->aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToSerialNumbersGet: ', $e->getMessage(), PHP_EOL;
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

## `cancelItemPost()`

```php
cancelItemPost($material_document_year, $material_document, $material_document_item, $posting_date): \BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentItemType
```

Cancels a material document item

Cancels a material document item that you specify by the material document number, year and item number.

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material_document_year = 'material_document_year_example'; // string | Material Doc. Year   (Value needs to be enclosed in single quotes)
$material_document = 'material_document_example'; // string | Material Document   (Value needs to be enclosed in single quotes)
$material_document_item = 'material_document_item_example'; // string | Material Doc.Item   (Value needs to be enclosed in single quotes)
$posting_date = 'posting_date_example'; // string | Posting Date   (Value needs to be enclosed in single quotes and prefixed with `datetime`, e.g. `datetime'2017-12-31T00:00'`)

try {
    $result = $apiInstance->cancelItemPost($material_document_year, $material_document, $material_document_item, $posting_date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentItemsApi->cancelItemPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material_document_year** | **string**| Material Doc. Year   (Value needs to be enclosed in single quotes) | |
| **material_document** | **string**| Material Document   (Value needs to be enclosed in single quotes) | |
| **material_document_item** | **string**| Material Doc.Item   (Value needs to be enclosed in single quotes) | |
| **posting_date** | **string**| Posting Date   (Value needs to be enclosed in single quotes and prefixed with &#x60;datetime&#x60;, e.g. &#x60;datetime&#39;2017-12-31T00:00&#39;&#x60;) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentItemType**](../Model/AMaterialDocumentItemType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
