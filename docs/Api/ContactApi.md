# Swagger\Client\ContactApi

All URIs are relative to *https://services.message-business.com/api/rest/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**contactDeleteContactById**](ContactApi.md#contactDeleteContactById) | **DELETE** /contact/attributebycid/{id} | Supprimer définitivement un contact
[**contactDeleteContactByKey**](ContactApi.md#contactDeleteContactByKey) | **DELETE** /contact/attribute/{contactKey} | Supprimer définitivement un contact
[**contactGetContacHistory**](ContactApi.md#contactGetContacHistory) | **GET** /contact/history/{contactKey}/{size} | Obtenir la liste des activités d&#39;un contact
[**contactGetContactAttributeId**](ContactApi.md#contactGetContactAttributeId) | **GET** /contact/attributebycid/{id} | Obtenir la liste des champs et leur valeur
[**contactGetContactAttributeIdKey**](ContactApi.md#contactGetContactAttributeIdKey) | **GET** /contact/attributevalueid/{contactKey} | Obtenir une valeur spécifique avec la clé d&#39;unicité
[**contactGetContactAttributeIdbyId**](ContactApi.md#contactGetContactAttributeIdbyId) | **GET** /contact/attributevalueidbycid/{id} | Obtenir un champ et sa valeur
[**contactGetContactAttributeKey**](ContactApi.md#contactGetContactAttributeKey) | **GET** /contact/attribute/{contactKey} | Obtenir la liste des informations d&#39;un contact
[**contactPostContacHistory**](ContactApi.md#contactPostContacHistory) | **POST** /contact/history | Ajouter une activité à un contact suite à une opération
[**contactPostContactAttributeKey**](ContactApi.md#contactPostContactAttributeKey) | **POST** /contact/attribute | Créer ou mettre à jour les informations d&#39;un contact
[**contactPutContactAttributeKey**](ContactApi.md#contactPutContactAttributeKey) | **PUT** /contact/attribute | Mettre à jour des informations du contact


# **contactDeleteContactById**
> string contactDeleteContactById($id)

Supprimer définitivement un contact

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 

try {
    $result = $apiInstance->contactDeleteContactById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactDeleteContactById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactDeleteContactByKey**
> string contactDeleteContactByKey($contact_key)

Supprimer définitivement un contact

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_key = "contact_key_example"; // string | 

try {
    $result = $apiInstance->contactDeleteContactByKey($contact_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactDeleteContactByKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_key** | **string**|  |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactGetContacHistory**
> \Swagger\Client\Model\ContactHistory contactGetContacHistory($contact_key, $size)

Obtenir la liste des activités d'un contact

Par defaut, les 50 dernières activitées du contact sont renvoyées. Vous pouvez laisser ce champ vide

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_key = "contact_key_example"; // string | 
$size = 56; // int | 

try {
    $result = $apiInstance->contactGetContacHistory($contact_key, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactGetContacHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_key** | **string**|  |
 **size** | **int**|  |

### Return type

[**\Swagger\Client\Model\ContactHistory**](../Model/ContactHistory.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactGetContactAttributeId**
> \Swagger\Client\Model\ContactData[] contactGetContactAttributeId($id)

Obtenir la liste des champs et leur valeur

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | contact id

try {
    $result = $apiInstance->contactGetContactAttributeId($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactGetContactAttributeId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| contact id |

### Return type

[**\Swagger\Client\Model\ContactData[]**](../Model/ContactData.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactGetContactAttributeIdKey**
> \Swagger\Client\Model\ContactData[] contactGetContactAttributeIdKey($contact_key)

Obtenir une valeur spécifique avec la clé d'unicité

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_key = "contact_key_example"; // string | Clé d'unicité

try {
    $result = $apiInstance->contactGetContactAttributeIdKey($contact_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactGetContactAttributeIdKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_key** | **string**| Clé d&#39;unicité |

### Return type

[**\Swagger\Client\Model\ContactData[]**](../Model/ContactData.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactGetContactAttributeIdbyId**
> \Swagger\Client\Model\ContactData[] contactGetContactAttributeIdbyId($id)

Obtenir un champ et sa valeur

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | contact id

try {
    $result = $apiInstance->contactGetContactAttributeIdbyId($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactGetContactAttributeIdbyId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| contact id |

### Return type

[**\Swagger\Client\Model\ContactData[]**](../Model/ContactData.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactGetContactAttributeKey**
> \Swagger\Client\Model\ContactData[] contactGetContactAttributeKey($contact_key)

Obtenir la liste des informations d'un contact

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_key = "contact_key_example"; // string | Clé d'unicité

try {
    $result = $apiInstance->contactGetContactAttributeKey($contact_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactGetContactAttributeKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_key** | **string**| Clé d&#39;unicité |

### Return type

[**\Swagger\Client\Model\ContactData[]**](../Model/ContactData.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactPostContacHistory**
> string contactPostContacHistory($contact_history)

Ajouter une activité à un contact suite à une opération

##### Informations sur ContactHistory #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | contactKey   | Ceci est la clé d'unicité actuellement paramétrée sur le compte                      |  | contactFound | La valeur est ignorée                                                         |  | records      | La valeur est ignorée                                                         |  | logs         | Ceci est la liste des activités que vous souhaitez enregistrer                  |    ##### Informations sur ContactLog #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | Id           | La valeur est ignorée                                                         |  | Type         | La valeur est ignorée                                                         |  | Object       | La valeur est ignorée                                                         |  | Title        | Titre (affiché dans l'interface)                                                               |  | Date         | La valeur est ignorée                                                         |  | Group        | La valeur est ignorée                                                         |  | OperationId  | L'id de l'opération que vous souhaité affecté a ce log. Important pour les triggers      |  | LogDate      | La date de l'activité est enregistrée est au format de date UTC \"yyyy-MM-dd HH:mm:ss+0000\", make sure you add the +0000 to make it a UTC hour |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_history = new \Swagger\Client\Model\ContactHistory(); // \Swagger\Client\Model\ContactHistory | Modèle de ContactHistory

try {
    $result = $apiInstance->contactPostContacHistory($contact_history);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactPostContacHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_history** | [**\Swagger\Client\Model\ContactHistory**](../Model/ContactHistory.md)| Modèle de ContactHistory |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactPostContactAttributeKey**
> string contactPostContactAttributeKey($contact_data)

Créer ou mettre à jour les informations d'un contact

Si vous avez un champ de type MultipleSelection vous devrez insérer les id d'attributs separés par des \",\"  Ex: \"53,54\" où 53 et 54 sont l'id de l'attribute values (vous pouvez avoir les id en faisant un appel à GET /account/contactattribute/value/{id}    ##### Informations sur ContactData #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | La valeur est ignorée                                                         |  | contactKey   | Ceci est le champ de clé d'unicité de la base                                       |  | attributes   | La liste des champs d'un contact. Voir ContactAttribute en dessous         |    ##### Informations sur ContactAttribute #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | Le nom du champ (voir en dessous) -  Vous devez utiliser ce champs pour faire une insertion / mise à jour de la valeure     |  | fieldName    | Le nom du champ (voir en dessous) - Vous ne devez pas utiliser ce champ pour faire une insertion / mise à jour de la valeur |  | fieldValue   | La valeur donnée au champ (voir en dessous)                           |    #### Information sur le nom des champs et leurs valeurs  | Liste des noms possible        | Type de valeur                                                 |  |------------------------------|---------------------------------------------------------------|  | \"salutation\", \"firstname\", \"lastname\", \"companyname\", \"jobtitle\" | Type string libre |  | \"email\", \"emailunsubscriptionreason\", \"emailstatus\" | Type string libre |  | \"emailstatusdetail\", \"emailcapping\", \"mobile\"  | Type string libre |  | \"mobileunsubscriptionreason\", \"mobilestatus\", \"mobilestatusdetail\" | Type string libre |  | \"mobilecapping\", \"phone\", \"fax\", \"address1\", \"address2\"  | Type string libre |  | \"zipcode\", \"city\", \"country\",  \"type\" | Type string libre |  | \"activity\", \"comments\", \"source\", \"activityrank\", \"influencerank\" | Type string libre |  | \"emailunsubscriptiondate\", \"emailstatusdate\", \"mobileunsubscriptiondate\", \"mobilestatusdate\" | Un type string au format UTC \"yyyy-MM-dd HH:mm:ss+0000\" |  | \"emailoptinpartners\", \"mobileoptinpartners\", \"emailoptin\", \"mobileoptin\" | Un type string comme \"true\" ou \"yes1\" ou \"no\"  |  | {Personalised_id}  | Type string libre  |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_data = new \Swagger\Client\Model\ContactData(); // \Swagger\Client\Model\ContactData | Données du contact

try {
    $result = $apiInstance->contactPostContactAttributeKey($contact_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactPostContactAttributeKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_data** | [**\Swagger\Client\Model\ContactData**](../Model/ContactData.md)| Données du contact |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contactPutContactAttributeKey**
> string contactPutContactAttributeKey($contact_data)

Mettre à jour des informations du contact

Si vous avez un champ de type MultipleSelection vous devrez insérer les id d'attributs separés par des \",\"  Ex: \"53,54\" où 53 et 54 sont l'id de l'attribute values (vous pouvez avoir les id en faisant un appel à GET /account/contactattribute/value/{id})    ##### Informations sur ContactData #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | Si un id est fourni, celui-ci sera utilisé pour récupérer le contact          |  | contactKey   | Ceci est le champ de clé d'unicité de la base (ignoré si l'id est fourni)           |  | attributes   | La liste des champs d'un contact. Voir ContactAttribute en dessous         |    ##### Informations sur ContactAttribute #####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | Le nom du champ (voir en dessous) -  Vous devez utiliser ce champs pour faire une insertion / mise à jour de la valeure     |  | fieldName    | Le nom du champ (voir en dessous)                                                    |  | fieldValue   | La valeur donnée au champ (voir en dessous)                           |    #### Information sur le nom des champs et leurs valeurs   | Liste des noms possible        | Type de valeur                                                 |  |------------------------------|---------------------------------------------------------------|  | \"salutation\", \"firstname\", \"lastname\", \"companyname\", \"jobtitle\" | Type string libre |  | \"email\", \"emailunsubscriptionreason\", \"emailstatus\" | Type string libre |  | \"emailstatusdetail\", \"emailcapping\", \"mobile\"  | Type string libre |  | \"mobileunsubscriptionreason\", \"mobilestatus\", \"mobilestatusdetail\" | Type string libre |  | \"mobilecapping\", \"phone\", \"fax\", \"address1\", \"address2\"  | Type string libre |  | \"zipcode\", \"city\", \"country\",  \"type\" | Type string libre |  | \"activity\", \"comments\", \"source\", \"activityrank\", \"influencerank\" | Type string libre |  | \"emailunsubscriptiondate\", \"emailstatusdate\", \"mobileunsubscriptiondate\", \"mobilestatusdate\" | Un type string au format UTC \"yyyy-MM-dd HH:mm:ss+0000\" |  | \"emailoptinpartners\", \"mobileoptinpartners\", \"emailoptin\", \"mobileoptin\" | Un type string comme \"true\" ou \"yes1\" ou \"no\"  |  | {Personalised_id}  | Type string libre  |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\ContactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_data = new \Swagger\Client\Model\ContactData(); // \Swagger\Client\Model\ContactData | Données du contact

try {
    $result = $apiInstance->contactPutContactAttributeKey($contact_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactApi->contactPutContactAttributeKey: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_data** | [**\Swagger\Client\Model\ContactData**](../Model/ContactData.md)| Données du contact |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

