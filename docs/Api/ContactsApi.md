# Swagger\Client\ContactsApi

All URIs are relative to *https://services.message-business.com/api/rest/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**contactsDeleteDelete**](ContactsApi.md#contactsDeleteDelete) | **DELETE** /contacts/purge/{id} | Supprimer définitivement une précédente purge
[**contactsDeleteExport**](ContactsApi.md#contactsDeleteExport) | **DELETE** /contacts/export/{id} | Supprimer définitivement un export
[**contactsDeleteImport**](ContactsApi.md#contactsDeleteImport) | **DELETE** /contacts/import/{id} | Supprimer définitivement les information d&#39;un précedent import
[**contactsGetDelete**](ContactsApi.md#contactsGetDelete) | **GET** /contacts/purge/{id} | Obtenir les informations d&#39;une précédente purge
[**contactsGetDeleteList**](ContactsApi.md#contactsGetDeleteList) | **GET** /contacts/purge | Obtenir la liste des précédentes purges
[**contactsGetExport**](ContactsApi.md#contactsGetExport) | **GET** /contacts/export/{id} | Obtenir les informations d&#39;un précédent export
[**contactsGetExportList**](ContactsApi.md#contactsGetExportList) | **GET** /contacts/export | Obtenir la liste des précédents exports
[**contactsGetFileDelete**](ContactsApi.md#contactsGetFileDelete) | **GET** /contacts/purge/file/{fileName} | Télécharger le fichier d&#39;archive de la purge
[**contactsGetFileExport**](ContactsApi.md#contactsGetFileExport) | **GET** /contacts/export/file/{fileName} | Télécharger le fichier d&#39;archive de l&#39;export
[**contactsGetFileImport**](ContactsApi.md#contactsGetFileImport) | **GET** /contacts/import/file/{fileName} | Télécharger le fichier d&#39;archive d&#39;un import
[**contactsGetImport**](ContactsApi.md#contactsGetImport) | **GET** /contacts/import/{id} | Obtenir les informations d&#39;un précédent import
[**contactsGetImportList**](ContactsApi.md#contactsGetImportList) | **GET** /contacts/import | Obtenir la liste des précédents imports
[**contactsPostContactsAttributeKey**](ContactsApi.md#contactsPostContactsAttributeKey) | **POST** /contacts/attribute | Créer ou mettre à jour des informations de contacts (jusqu&#39;à 500)
[**contactsPostDeleteOperation**](ContactsApi.md#contactsPostDeleteOperation) | **POST** /contacts/purge/add | Effectuer une purge à partir d&#39;un fichier
[**contactsPostExportOperation**](ContactsApi.md#contactsPostExportOperation) | **POST** /contacts/export/add | Lancer un nouvel export de la base de contact
[**contactsPostImportOperation**](ContactsApi.md#contactsPostImportOperation) | **POST** /contacts/import/add | Effectuer un nouvel import dans la base de contacts
[**contactsPutContactAttributeKey**](ContactsApi.md#contactsPutContactAttributeKey) | **PUT** /contacts/attribute | Mettre à jour des informations de contacts (jusqu&#39;à 500)


# **contactsDeleteDelete**
> string contactsDeleteDelete($id)

Supprimer définitivement une précédente purge

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | L'id de la purge

try {
    $result = $apiInstance->contactsDeleteDelete($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsDeleteDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| L&#39;id de la purge |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsDeleteExport**
> string contactsDeleteExport($id)

Supprimer définitivement un export

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | L'id de l'opération d'export

try {
    $result = $apiInstance->contactsDeleteExport($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsDeleteExport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| L&#39;id de l&#39;opération d&#39;export |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsDeleteImport**
> string contactsDeleteImport($id)

Supprimer définitivement les information d'un précedent import

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The import operation id

try {
    $result = $apiInstance->contactsDeleteImport($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsDeleteImport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The import operation id |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsGetDelete**
> \Swagger\Client\Model\PurgeOperation contactsGetDelete($id)

Obtenir les informations d'une précédente purge

Link indique l'url où télécharger le fichier d'archive une fois disponible

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | L'id de la purge

try {
    $result = $apiInstance->contactsGetDelete($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsGetDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| L&#39;id de la purge |

### Return type

[**\Swagger\Client\Model\PurgeOperation**](../Model/PurgeOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsGetDeleteList**
> \Swagger\Client\Model\PurgeOperation[] contactsGetDeleteList()

Obtenir la liste des précédentes purges

Link indique l'url où télécharger le fichier d'archive une fois disponible

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->contactsGetDeleteList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsGetDeleteList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\PurgeOperation[]**](../Model/PurgeOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsGetExport**
> \Swagger\Client\Model\ExportOperation contactsGetExport($id)

Obtenir les informations d'un précédent export

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | L'id de l'opération d'export

try {
    $result = $apiInstance->contactsGetExport($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsGetExport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| L&#39;id de l&#39;opération d&#39;export |

### Return type

[**\Swagger\Client\Model\ExportOperation**](../Model/ExportOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsGetExportList**
> \Swagger\Client\Model\ExportOperation[] contactsGetExportList()

Obtenir la liste des précédents exports

Link indique l'url où télécharger le fichier d'archive une fois disponible

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->contactsGetExportList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsGetExportList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\ExportOperation[]**](../Model/ExportOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsGetFileDelete**
> \SplFileObject contactsGetFileDelete($file_name)

Télécharger le fichier d'archive de la purge

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file_name = "file_name_example"; // string | Nom du fichier d'archive

try {
    $result = $apiInstance->contactsGetFileDelete($file_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsGetFileDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_name** | **string**| Nom du fichier d&#39;archive |

### Return type

[**\SplFileObject**](../Model/\SplFileObject.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsGetFileExport**
> \SplFileObject contactsGetFileExport($file_name)

Télécharger le fichier d'archive de l'export

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file_name = "file_name_example"; // string | Nom du fichier d'archive

try {
    $result = $apiInstance->contactsGetFileExport($file_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsGetFileExport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_name** | **string**| Nom du fichier d&#39;archive |

### Return type

[**\SplFileObject**](../Model/\SplFileObject.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsGetFileImport**
> \SplFileObject contactsGetFileImport($file_name)

Télécharger le fichier d'archive d'un import

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file_name = "file_name_example"; // string | Nom du fichier d'archive

try {
    $result = $apiInstance->contactsGetFileImport($file_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsGetFileImport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_name** | **string**| Nom du fichier d&#39;archive |

### Return type

[**\SplFileObject**](../Model/\SplFileObject.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsGetImport**
> \Swagger\Client\Model\ImportOperation contactsGetImport($id)

Obtenir les informations d'un précédent import

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The import operation id

try {
    $result = $apiInstance->contactsGetImport($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsGetImport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The import operation id |

### Return type

[**\Swagger\Client\Model\ImportOperation**](../Model/ImportOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsGetImportList**
> \Swagger\Client\Model\ImportOperation[] contactsGetImportList()

Obtenir la liste des précédents imports

Link indique l'url où télécharger le fichier d'archive une fois disponible

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->contactsGetImportList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsGetImportList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\ImportOperation[]**](../Model/ImportOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsPostContactsAttributeKey**
> string contactsPostContactsAttributeKey($contacts_data)

Créer ou mettre à jour des informations de contacts (jusqu'à 500)

##### Informations sur ContactData #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | La valeur est ignorée                                                         |  | contactKey   | Ceci est le champ de clé d'unicité de la base                                       |  | attributes   | La liste des champs d'un contact. Voir ContactAttribute en dessous         |    ##### Informations sur ContactAttribute #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | Le nom du champ (voir en dessous) -  Vous devez utiliser ce champs pour faire une insertion / mise à jour de la valeure     |  | fieldName    | Le nom du champ (voir en dessous)                                                    |  | fieldValue   | La valeur donnée au champ (voir en dessous)                           |    #### Information sur le nom des champs et leurs valeurs  | Liste des noms possible        | Type de valeur                                                 |  |------------------------------|---------------------------------------------------------------|  | \"salutation\", \"firstname\", \"lastname\", \"companyname\", \"jobtitle\" | Type string libre |  | \"email\", \"emailunsubscriptionreason\", \"emailstatus\" | Type string libre |  | \"emailstatusdetail\", \"emailcapping\", \"mobile\"  | Type string libre |  | \"mobileunsubscriptionreason\", \"mobilestatus\", \"mobilestatusdetail\" | Type string libre |  | \"mobilecapping\", \"phone\", \"fax\", \"address1\", \"address2\"  | Type string libre |  | \"zipcode\", \"city\", \"country\",  \"type\" | Type string libre |  | \"activity\", \"comments\", \"source\", \"activityrank\", \"influencerank\" | Type string libre |  | \"emailunsubscriptiondate\", \"emailstatusdate\", \"mobileunsubscriptiondate\", \"mobilestatusdate\" | Un type string au format UTC \"yyyy-MM-dd HH:mm:ss+0000\" |  | \"emailoptinpartners\", \"mobileoptinpartners\", \"emailoptin\", \"mobileoptin\" | Un type string comme \"true\" ou \"yes1\" ou \"no\"  |  | {Personalised_id}  | Type string libre  |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contacts_data = array(new \Swagger\Client\Model\ContactData()); // \Swagger\Client\Model\ContactData[] | Données du contact

try {
    $result = $apiInstance->contactsPostContactsAttributeKey($contacts_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsPostContactsAttributeKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contacts_data** | [**\Swagger\Client\Model\ContactData[]**](../Model/ContactData.md)| Données du contact |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsPostDeleteOperation**
> \Swagger\Client\Model\PurgeOperation contactsPostDeleteOperation($first_line, $first_line_as_header, $encoding, $separator, $key_column, $file)

Effectuer une purge à partir d'un fichier

##### Informations sur les champs #####    - **firstLine** doit être supérieur à 1  - **firstLineAs** un entête avec comme valeur \"true\" ou \"false\"  - **encoding** peut être \"UTF-8\", \"Unicode\", \"ISO-8859-1\", \"ISO-8859-15\", \"UTF-32\", \"UTF-7\"  - **separator** peut être ',', ';', ' ',  '\\t', '-', '|', '*', ':', '.', '&amp;', '/', '\\', '+', '\"'  - **keyColumn** est le nombre indiquant la colonne du fichier incluant la clé d'unicité des contacts à supprimer dans la base   - **file** est le fichier (.txt, .csv) à utiliser pour la purge

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$first_line = 56; // int | 
$first_line_as_header = "first_line_as_header_example"; // string | 
$encoding = "encoding_example"; // string | 
$separator = "separator_example"; // string | 
$key_column = 56; // int | 
$file = "/path/to/file.txt"; // \SplFileObject | 

try {
    $result = $apiInstance->contactsPostDeleteOperation($first_line, $first_line_as_header, $encoding, $separator, $key_column, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsPostDeleteOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **first_line** | **int**|  |
 **first_line_as_header** | **string**|  |
 **encoding** | **string**|  |
 **separator** | **string**|  |
 **key_column** | **int**|  |
 **file** | **\SplFileObject**|  |

### Return type

[**\Swagger\Client\Model\PurgeOperation**](../Model/PurgeOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsPostExportOperation**
> \Swagger\Client\Model\ExportOperation contactsPostExportOperation($export_nfo)

Lancer un nouvel export de la base de contact

##### Informations sur ContactExportNfo #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | name           | Le nom qui sera affiché sur votre interface                                   |  | description   | Indiquez segment:&lt;id_du_segment&gt; pour ajouter un export d'un segment particulier plutôt que l'ensemble des contacts|  | fields   | \"salutation\", \"firstname\", \"lastname\", \"companyname\", \"jobtitle\", \"email\", \"emailoptin\", \"emailunsubscriptiondate\", \"emailunsubscriptionreason\", \"emailstatus\", \"emailstatusdate\", \"emailstatusdetail\", \"emailcapping\", \"mobile\", \"mobileoptin\", \"mobileunsubscriptiondate\", \"mobileunsubscriptionreason\", \"mobilestatus\", \"mobilestatusdate\", \"mobilestatusdetail\", \"mobilecapping\", \"phone\", \"fax\", \"address1\", \"address2\", \"zipcode\", \"city\", \"country\", \"emailoptinpartners\", \"mobileoptinpartners\", \"creationdate\", \"importcreation\", \"modificationdate\", \"importmodification\", \"type\", \"activity\", \"comments\", \"source\", \"activityrank\", \"remotedate\", \"remoteos\", \"remoteip\", \"remoteuamail\", \"remoteuaweb\", \"emailopenings\", \"emailopeninglastdate\", \"emailopeninglastname\", \"emailclicks\", \"emailclickinglastdate\", \"emailclickinglastname\", \"emailclickinglastlink\", \"{Personalised_id}\"  |  | filters   | \"emailingoptin\", \"mobileoptin\", \"emailingoptout\", \"mobileoptout\", \"emailingsoft\", \"emailinghard\" |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$export_nfo = new \Swagger\Client\Model\ContactExportNfo(); // \Swagger\Client\Model\ContactExportNfo | Modèle de ContactExportNfo

try {
    $result = $apiInstance->contactsPostExportOperation($export_nfo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsPostExportOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **export_nfo** | [**\Swagger\Client\Model\ContactExportNfo**](../Model/ContactExportNfo.md)| Modèle de ContactExportNfo |

### Return type

[**\Swagger\Client\Model\ExportOperation**](../Model/ExportOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsPostImportOperation**
> \Swagger\Client\Model\ImportOperation contactsPostImportOperation($name, $first_line, $first_line_as_header, $encoding, $separator, $duplicate_option, $matchings, $file)

Effectuer un nouvel import dans la base de contacts

##### Informations sur les champs #####    - **firstLine** doit être supérieur à 1  - **firstLineAs** un entête avec comme valeur \"true\" ou \"false\"  - **encoding** peut être \"UTF-8\", \"Unicode\", \"ISO-8859-1\", \"ISO-8859-15\", \"UTF-32\", \"UTF-7\"  - **separator** peut être ',', ';', ' ',  '\\t', '-', '|', '*', ':', '.', '&amp;', '/', '\\', '+', '\"'  - **duplicateOption** peut être \"disallowdupupdate\", \"disallowdup\", \"allowdup\"  - **matchings** est un tableau de type string décrit ci dessous  - **file** est le fichier (.txt, .csv) à utiliser pour la purge    Le POST doit avoir comment content-type:  multipart/form-data  Il faut aussi que la variable matching soit sous la forme d'un tableau ex: [\"email\", \"firstname\"]    ##### Détail des différentes options de duplicateOption #####    disallowdupupdate: Mettre à jour les informations de votre Base Contacts par celles du fichier.    disallowdup: N'importer dans la Base Contacts que les nouveaux Contacts du fichier. Les Contacts déjà présents dans votre Base ne seront pas modifiés..    allowdup: Cette option n'est possible que si la paramètre de la base de contact du compte est positionné sur l'autorisation d'avoir des doublons (non-recommandé) dans la base de contacts.    ##### Les valeurs correspondantes possibles #####    | Liste des valeurs |  |----------------|  | \"firstname\", \"lastname\", \"companyname\", \"email\", \"emailoptin\", \"emailstatus\", \"mobile\", \"mobileoptin\", \"mobilestatus\", \"phone\" |  | \"salutation\", \"jobtitle\", \"fax\", \"address1\", \"address2\", \"zipcode\", \"city\", \"country\", \"emailoptinpartners\", \"mobileoptinpartners\", \"type\", \"activity\", \"comments\", \"source\" |  | {Personalised_id} |    L'id de personalisation peut être trouvé dans votre compte Sendethic, vous devez mettre l'id ex: \"26\"

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$name = "name_example"; // string | 
$first_line = 56; // int | 
$first_line_as_header = "first_line_as_header_example"; // string | 
$encoding = "encoding_example"; // string | 
$separator = "separator_example"; // string | 
$duplicate_option = "duplicate_option_example"; // string | 
$matchings = "matchings_example"; // string | 
$file = "/path/to/file.txt"; // \SplFileObject | 

try {
    $result = $apiInstance->contactsPostImportOperation($name, $first_line, $first_line_as_header, $encoding, $separator, $duplicate_option, $matchings, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsPostImportOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**|  |
 **first_line** | **int**|  |
 **first_line_as_header** | **string**|  |
 **encoding** | **string**|  |
 **separator** | **string**|  |
 **duplicate_option** | **string**|  |
 **matchings** | **string**|  |
 **file** | **\SplFileObject**|  |

### Return type

[**\Swagger\Client\Model\ImportOperation**](../Model/ImportOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactsPutContactAttributeKey**
> string contactsPutContactAttributeKey($contacts_data)

Mettre à jour des informations de contacts (jusqu'à 500)

##### Informations sur ContactData #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | La valeur est ignorée             |  | contactKey   | Ceci est le champ de clé d'unicité de la base                                       |  | attributes   | La liste des champs d'un contact. Voir ContactAttribute en dessous         |    ##### Informations sur ContactAttribute #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | Le nom du champ (voir en dessous) -  Vous devez utiliser ce champs pour faire une insertion / mise à jour de la valeure     |  | fieldName    | Le nom du champ (voir en dessous)                                                    |  | fieldValue   | La valeur donnée au champ (voir en dessous)                           |    #### Information sur le nom des champs et leurs valeurs   | Liste des noms possible        | Type de valeur                                                 |  |------------------------------|---------------------------------------------------------------|  | \"salutation\", \"firstname\", \"lastname\", \"companyname\", \"jobtitle\" | Type string libre |  | \"email\", \"emailunsubscriptionreason\", \"emailstatus\" | Type string libre |  | \"emailstatusdetail\", \"emailcapping\", \"mobile\"  | Type string libre |  | \"mobileunsubscriptionreason\", \"mobilestatus\", \"mobilestatusdetail\" | Type string libre |  | \"mobilecapping\", \"phone\", \"fax\", \"address1\", \"address2\"  | Type string libre |  | \"zipcode\", \"city\", \"country\",  \"type\" | Type string libre |  | \"activity\", \"comments\", \"source\", \"activityrank\", \"influencerank\" | Type string libre |  | \"emailunsubscriptiondate\", \"emailstatusdate\", \"mobileunsubscriptiondate\", \"mobilestatusdate\" | Un type string au format UTC \"yyyy-MM-dd HH:mm:ss+0000\" |  | \"emailoptinpartners\", \"mobileoptinpartners\", \"emailoptin\", \"mobileoptin\" | Un type string comme \"true\" ou \"yes1\" ou \"no\"  |  | {Personalised_id}  | Type string libre  |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contacts_data = array(new \Swagger\Client\Model\ContactData()); // \Swagger\Client\Model\ContactData[] | Données du contact

try {
    $result = $apiInstance->contactsPutContactAttributeKey($contacts_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contactsPutContactAttributeKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contacts_data** | [**\Swagger\Client\Model\ContactData[]**](../Model/ContactData.md)| Données du contact |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

