# BeLenka\SAP\MaterialDocument\DocumentHeaderApi

All URIs are relative to https://:/sap/opu/odata/sap/API_MATERIAL_DOCUMENT_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aMaterialDocumentHeaderGet()**](DocumentHeaderApi.md#aMaterialDocumentHeaderGet) | **GET** /A_MaterialDocumentHeader | Reads information on material document header level |
| [**aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentGet()**](DocumentHeaderApi.md#aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentGet) | **GET** /A_MaterialDocumentHeader(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;) | Reads information for a specific material document header |
| [**aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet()**](DocumentHeaderApi.md#aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet) | **GET** /A_MaterialDocumentHeader(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;)/to_MaterialDocumentItem | Reads information for a specific material document header and material document items |
| [**aMaterialDocumentHeaderPost()**](DocumentHeaderApi.md#aMaterialDocumentHeaderPost) | **POST** /A_MaterialDocumentHeader | Creates a material document |
| [**aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet()**](DocumentHeaderApi.md#aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet) | **GET** /A_MaterialDocumentItem(MaterialDocumentYear&#x3D;&#39;{MaterialDocumentYear}&#39;,MaterialDocument&#x3D;&#39;{MaterialDocument}&#39;,MaterialDocumentItem&#x3D;&#39;{MaterialDocumentItem}&#39;)/to_MaterialDocumentHeader | Reads information on material document item and header level for a specific material document item |
| [**cancelPost()**](DocumentHeaderApi.md#cancelPost) | **POST** /Cancel | Cancels a material document |


## `aMaterialDocumentHeaderGet()`

```php
aMaterialDocumentHeaderGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\MaterialDocument\Model\Wrapper
```

Reads information on material document header level

Reads material document header information to get an overview of the material document postings.

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentHeaderApi(
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
    $result = $apiInstance->aMaterialDocumentHeaderGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentHeaderApi->aMaterialDocumentHeaderGet: ', $e->getMessage(), PHP_EOL;
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

[**\BeLenka\SAP\MaterialDocument\Model\Wrapper**](../Model/Wrapper.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentGet()`

```php
aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentGet($material_document_year, $material_document, $select, $expand): \BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentHeaderType
```

Reads information for a specific material document header

Reads material document header information for a specific material document to get an overview of the material document posting.

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material_document_year = 'material_document_year_example'; // string | Material Document Year
$material_document = 'material_document_example'; // string | Number of Material Document
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentGet($material_document_year, $material_document, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentHeaderApi->aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material_document_year** | **string**| Material Document Year | |
| **material_document** | **string**| Number of Material Document | |
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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentHeaderApi(
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
    echo 'Exception when calling DocumentHeaderApi->aMaterialDocumentHeaderMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentToMaterialDocumentItemGet: ', $e->getMessage(), PHP_EOL;
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

## `aMaterialDocumentHeaderPost()`

```php
aMaterialDocumentHeaderPost($apimaterialdocumentsrva_material_document_header_type_create): \BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentHeaderType
```

Creates a material document

Creates a material document compost by header and item for a specific business process.

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$apimaterialdocumentsrva_material_document_header_type_create = new \BeLenka\SAP\MaterialDocument\Model\APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreate(); // \BeLenka\SAP\MaterialDocument\Model\APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreate | New entity

try {
    $result = $apiInstance->aMaterialDocumentHeaderPost($apimaterialdocumentsrva_material_document_header_type_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentHeaderApi->aMaterialDocumentHeaderPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **apimaterialdocumentsrva_material_document_header_type_create** | [**\BeLenka\SAP\MaterialDocument\Model\APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreate**](../Model/APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreate.md)| New entity | |

### Return type

[**\BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentHeaderType**](../Model/AMaterialDocumentHeaderType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: `application/json`
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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentHeaderApi(
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
    echo 'Exception when calling DocumentHeaderApi->aMaterialDocumentItemMaterialDocumentYearMaterialDocumentYearMaterialDocumentMaterialDocumentMaterialDocumentItemMaterialDocumentItemToMaterialDocumentHeaderGet: ', $e->getMessage(), PHP_EOL;
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

## `cancelPost()`

```php
cancelPost($material_document_year, $material_document, $posting_date): \BeLenka\SAP\MaterialDocument\Model\AMaterialDocumentHeaderType
```

Cancels a material document

Cancels a complete material document that you specify by the material document number and year.

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


$apiInstance = new BeLenka\SAP\MaterialDocument\Api\DocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material_document_year = 'material_document_year_example'; // string | Material Doc. Year   (Value needs to be enclosed in single quotes)
$material_document = 'material_document_example'; // string | Material Document   (Value needs to be enclosed in single quotes)
$posting_date = 'posting_date_example'; // string | Posting Date   (Value needs to be enclosed in single quotes and prefixed with `datetime`, e.g. `datetime'2017-12-31T00:00'`)

try {
    $result = $apiInstance->cancelPost($material_document_year, $material_document, $posting_date);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentHeaderApi->cancelPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material_document_year** | **string**| Material Doc. Year   (Value needs to be enclosed in single quotes) | |
| **material_document** | **string**| Material Document   (Value needs to be enclosed in single quotes) | |
| **posting_date** | **string**| Posting Date   (Value needs to be enclosed in single quotes and prefixed with &#x60;datetime&#x60;, e.g. &#x60;datetime&#39;2017-12-31T00:00&#39;&#x60;) | [optional] |

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
