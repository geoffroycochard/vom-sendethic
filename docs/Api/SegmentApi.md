# Swagger\Client\SegmentApi

All URIs are relative to *https://services.message-business.com/api/rest/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**segmentDeleteSegment**](SegmentApi.md#segmentDeleteSegment) | **DELETE** /segment/{id} | Supprimer définitivement un segment
[**segmentGetAllSegments**](SegmentApi.md#segmentGetAllSegments) | **GET** /segment | Obtenir la liste de segments
[**segmentGetSegment**](SegmentApi.md#segmentGetSegment) | **GET** /segment/{id} | Obtenir un segment
[**segmentPostSegment**](SegmentApi.md#segmentPostSegment) | **POST** /segment | Ajouter un nouveau segment
[**segmentPutSegment**](SegmentApi.md#segmentPutSegment) | **PUT** /segment | Mettre à jour d&#39;un segment
[**segmentUpdateSegmentCache**](SegmentApi.md#segmentUpdateSegmentCache) | **GET** /segment/updatecache/{id} | Mettre à jour le comptage du segment


# **segmentDeleteSegment**
> string segmentDeleteSegment($id)

Supprimer définitivement un segment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id du segment

try {
    $result = $apiInstance->segmentDeleteSegment($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SegmentApi->segmentDeleteSegment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id du segment |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **segmentGetAllSegments**
> \Swagger\Client\Model\Segment[] segmentGetAllSegments()

Obtenir la liste de segments

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->segmentGetAllSegments();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SegmentApi->segmentGetAllSegments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Segment[]**](../Model/Segment.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **segmentGetSegment**
> \Swagger\Client\Model\Segment segmentGetSegment($id)

Obtenir un segment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id du segment

try {
    $result = $apiInstance->segmentGetSegment($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SegmentApi->segmentGetSegment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id du segment |

### Return type

[**\Swagger\Client\Model\Segment**](../Model/Segment.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **segmentPostSegment**
> \Swagger\Client\Model\Segment segmentPostSegment($segment)

Ajouter un nouveau segment

##### Informations sur Segment #####    | paramètre        | Information / Valeur possible                                                |  |--------------|-----------------------------------------------------------------------------|  | id           | Cet identifiant sera ignoré                                                      |  | description  | Un texte décrivant votre segment                                              |  | creationDate | La date sera renseignée par défaut avec la date courante au moment de l'appel  |  | name         | Nom du segment affiché dans le compte                    |  | mode         | \"intersect\", \"union\"                                                         |  | details      | Un type string en xml décrit en bas                                   |  * Ceci est un exemple de details d'un segment (vous pouvez faire un GET sur un segment pour voir la structure)    &lt;Criterias&gt;  &lt;Criteria guid=\"ff551463-5614-4174-af40-f26c41942ee4\" reference=\"op-unsubscribing-emailing\" type=\"Operation\"   id=\"0,5,0\" op=\"unsubscribingemailing\" is=\"true\" value1=\"\" value2=\"\" /&gt;  &lt;Criteria guid =\"ff551463-5614-4174-af40-f26c41942ee5\" reference=\"op-unsubscribing-emailing\" type=\"Operation\"   id=\"0,5,0\" op=\"unsubscribingemailing\" is=\"true\" value1=\"\" value2=\"\" /&gt;  &lt;/Criterias&gt;

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$segment = new \Swagger\Client\Model\Segment(); // \Swagger\Client\Model\Segment | Segment model

try {
    $result = $apiInstance->segmentPostSegment($segment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SegmentApi->segmentPostSegment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **segment** | [**\Swagger\Client\Model\Segment**](../Model/Segment.md)| Segment model |

### Return type

[**\Swagger\Client\Model\Segment**](../Model/Segment.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **segmentPutSegment**
> string segmentPutSegment($segment)

Mettre à jour d'un segment

##### Informations sur Segment #####    | paramètre        | Information / Valeur possible                                                |  |--------------|-----------------------------------------------------------------------------|  | id           | L'id sera utilisé pour mettre à jour le segment                 |  | description  | Un texte décrivant votre segment                                              |  | creationDate | La date sera renseignée par défaut avec la date courante au moment de l'appel  |  | name         | Nom du segment affiché dans le compte                    |  | mode         | \"intersect\", \"union\"                                                         |  | details      | Un type string en xml (Regarder la description du POST pour plus de details)         |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$segment = new \Swagger\Client\Model\Segment(); // \Swagger\Client\Model\Segment | Segment model

try {
    $result = $apiInstance->segmentPutSegment($segment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SegmentApi->segmentPutSegment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **segment** | [**\Swagger\Client\Model\Segment**](../Model/Segment.md)| Segment model |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **segmentUpdateSegmentCache**
> string segmentUpdateSegmentCache($id)

Mettre à jour le comptage du segment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SegmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id du segment

try {
    $result = $apiInstance->segmentUpdateSegmentCache($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SegmentApi->segmentUpdateSegmentCache: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id du segment |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

