# Swagger\Client\AccountApi

All URIs are relative to *https://services.message-business.com/api/rest/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountDeleteContactAttribute**](AccountApi.md#accountDeleteContactAttribute) | **DELETE** /account/contactattribute/{id} | Supprimer définitivement un champ
[**accountDeleteContactAttributeValue**](AccountApi.md#accountDeleteContactAttributeValue) | **DELETE** /account/contactattribute/value/{id} | Supprimer définitivement une valeur d&#39;un champ
[**accountGetAccountCredits**](AccountApi.md#accountGetAccountCredits) | **GET** /account/remainingcredits/{type_name} | Obtenir les credits restant   Vous pouvez choisir entre transactional, sms ou marketing
[**accountGetAccountSettings**](AccountApi.md#accountGetAccountSettings) | **GET** /account/settingsattribute/{setting} | Get an account attribute field
[**accountGetAllContactAttribute**](AccountApi.md#accountGetAllContactAttribute) | **GET** /account/contactattribute | Obtenir la liste des champs de la base de contact
[**accountGetAllContactAttributeValues**](AccountApi.md#accountGetAllContactAttributeValues) | **GET** /account/contactattribute/value/{id} | Obtenir la valeur d&#39;un champ spécifique
[**accountGetContactAttribute**](AccountApi.md#accountGetContactAttribute) | **GET** /account/contactattribute/{id} | Obtenir les informations d&#39;un champ
[**accountPostAccountSettings**](AccountApi.md#accountPostAccountSettings) | **PUT** /account/settingsattribute | Update an account attributes fields
[**accountPostContactAttribute**](AccountApi.md#accountPostContactAttribute) | **POST** /account/contactattribute | Ajouter un nouveau champ dans la base contact
[**accountPostContactAttributeValue**](AccountApi.md#accountPostContactAttributeValue) | **POST** /account/contactattribute/value/{id} | Ajouter une nouvelle valeur pour le champ spécifié (sélection unique ou multiple seulement)
[**accountPutContactAttribute**](AccountApi.md#accountPutContactAttribute) | **PUT** /account/contactattribute | Mettre à jour le nom d&#39;un champ
[**accountPutContactAttributeValue**](AccountApi.md#accountPutContactAttributeValue) | **PUT** /account/contactattribute/value | Mettre à jour de la valeur du champ en changeant le nom et/ou l&#39;index


# **accountDeleteContactAttribute**
> string accountDeleteContactAttribute($id)

Supprimer définitivement un champ



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Id du champ

try {
    $result = $apiInstance->accountDeleteContactAttribute($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountDeleteContactAttribute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Id du champ |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountDeleteContactAttributeValue**
> string accountDeleteContactAttributeValue($id)

Supprimer définitivement une valeur d'un champ



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | L'id de la valeur du champ

try {
    $result = $apiInstance->accountDeleteContactAttributeValue($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountDeleteContactAttributeValue: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| L&#39;id de la valeur du champ |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountGetAccountCredits**
> \Swagger\Client\Model\CreditsInformation accountGetAccountCredits($type_name)

Obtenir les credits restant   Vous pouvez choisir entre transactional, sms ou marketing

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$type_name = "type_name_example"; // string | type de credit (transactional, sms, marketing)

try {
    $result = $apiInstance->accountGetAccountCredits($type_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetAccountCredits: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type_name** | **string**| type de credit (transactional, sms, marketing) |

### Return type

[**\Swagger\Client\Model\CreditsInformation**](../Model/CreditsInformation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountGetAccountSettings**
> string accountGetAccountSettings($setting)

Get an account attribute field

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$setting = "setting_example"; // string | setting name

try {
    $result = $apiInstance->accountGetAccountSettings($setting);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetAccountSettings: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **setting** | **string**| setting name |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountGetAllContactAttribute**
> \Swagger\Client\Model\ContactField[] accountGetAllContactAttribute()

Obtenir la liste des champs de la base de contact

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->accountGetAllContactAttribute();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetAllContactAttribute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\ContactField[]**](../Model/ContactField.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountGetAllContactAttributeValues**
> \Swagger\Client\Model\ContactFieldValue[] accountGetAllContactAttributeValues($id)

Obtenir la valeur d'un champ spécifique



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Id du champ

try {
    $result = $apiInstance->accountGetAllContactAttributeValues($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetAllContactAttributeValues: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Id du champ |

### Return type

[**\Swagger\Client\Model\ContactFieldValue[]**](../Model/ContactFieldValue.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountGetContactAttribute**
> \Swagger\Client\Model\ContactField accountGetContactAttribute($id)

Obtenir les informations d'un champ

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | identifiant du champ

try {
    $result = $apiInstance->accountGetContactAttribute($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetContactAttribute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| identifiant du champ |

### Return type

[**\Swagger\Client\Model\ContactField**](../Model/ContactField.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountPostAccountSettings**
> string accountPostAccountSettings($account_nfo)

Update an account attributes fields

##### SettingsInformation body notes #####    | paramètre        | Information / Valeur possible                                                          |  |--------------|---------------------------------------------------------------------------------------|  | attributeType           | {key, value} array                                                         |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_nfo = new \Swagger\Client\Model\SettingsInformation(); // \Swagger\Client\Model\SettingsInformation | SettingsInformation model

try {
    $result = $apiInstance->accountPostAccountSettings($account_nfo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountPostAccountSettings: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_nfo** | [**\Swagger\Client\Model\SettingsInformation**](../Model/SettingsInformation.md)| SettingsInformation model |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountPostContactAttribute**
> \Swagger\Client\Model\ContactField accountPostContactAttribute($contact_field)

Ajouter un nouveau champ dans la base contact

##### Informations sur ContactField #####    | paramètre        | Information / Valeur possible                                                |  |--------------|-----------------------------------------------------------------------------|  | id           | Cet identifiant sera ignoré                                                      |  | format       | \"DateTime\", \"MultipleSelection\", \"Number\", \"SingleSelection\", \"ShortText\"   |  | creationDate | Cette valeur doit être au format de date UTC \"yyyy-MM-dd HH:mm:ss\"                |  | options      | Ce champ est optionnel et dépend du champ format. Voir ci-dessous pour les valeurs possibles. |  | name         | Le nom de ce champ sera verifié pour vérifier si ce nom n'est pas déjà déclaré           |    #####  Options par type de format #####    | Format        | Information / Valeur possible                                                   |  |--------------|---------------------------------------------------------------------------------|  | DateTime        | \"yyyy.mm.dd\", \"yy.mm.dd\", \"dd.mm.yyyy\", \"dd.mm.yy\", \"mm.dd.yyyy\", \"mm.dd.yy\" |  | MultipleSelection | \"true\", \"false\" sur un fichier d'import si la valeur est à \"true\" les nouvelles valeurs seront ajoutées |  | SingleSelection   | \"true\", \"false\" sur un fichier d'import si la valeur est à \"true\" les nouvelles valeurs seront ajoutées |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_field = new \Swagger\Client\Model\ContactField(); // \Swagger\Client\Model\ContactField | Modèle de ContactField

try {
    $result = $apiInstance->accountPostContactAttribute($contact_field);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountPostContactAttribute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_field** | [**\Swagger\Client\Model\ContactField**](../Model/ContactField.md)| Modèle de ContactField |

### Return type

[**\Swagger\Client\Model\ContactField**](../Model/ContactField.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountPostContactAttributeValue**
> \Swagger\Client\Model\ContactFieldValue accountPostContactAttributeValue($id, $contact_field_value)

Ajouter une nouvelle valeur pour le champ spécifié (sélection unique ou multiple seulement)

##### Informations sur ContactFieldValue #####    | paramètre        | Information / Valeur possible                                                          |  |--------------|---------------------------------------------------------------------------------------|  | id           | Cet identifiant sera ignoré                                                                |  | creationDate | La date sera renseignée par défaut avec la date courante               |  | index        | Position où sera enregistrée la valeur (par défaut, en dernière position)           |   | text         | Le texte qui sera affiché pour cette valeur                                        |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | L'id du champ
$contact_field_value = new \Swagger\Client\Model\ContactFieldValue(); // \Swagger\Client\Model\ContactFieldValue | Modèle de ContactFieldValue

try {
    $result = $apiInstance->accountPostContactAttributeValue($id, $contact_field_value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountPostContactAttributeValue: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| L&#39;id du champ |
 **contact_field_value** | [**\Swagger\Client\Model\ContactFieldValue**](../Model/ContactFieldValue.md)| Modèle de ContactFieldValue |

### Return type

[**\Swagger\Client\Model\ContactFieldValue**](../Model/ContactFieldValue.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountPutContactAttribute**
> string accountPutContactAttribute($contact_field)

Mettre à jour le nom d'un champ

##### Informations sur ContactField #####    | paramètre        | Information / Valeur possible                                                |  |--------------|-----------------------------------------------------------------------------|  | id           | L'identifiant doit correspondre au champ que vous voulez mettre à jour                           |  | format       | Le format sera ignorée, il ne peut être changé                      |  | creationDate | La creationDate sera ignorée, elle ne peut être changée                |  | options      | Ce champ est optionnel et dépend du champ format. Voir ci-dessous pour les valeurs possibles. |  | name         | Le nom de ce champ sera verifié pour vérifier si ce nom n'est pas déjà déclaré           |    #####  Options par type de format #####    | Format        | Information / Valeur possible                                                   |  |--------------|---------------------------------------------------------------------------------|  | DateTime        | \"yyyy.mm.dd\", \"yy.mm.dd\", \"dd.mm.yyyy\", \"dd.mm.yy\", \"mm.dd.yyyy\", \"mm.dd.yy\" |  | MultipleSelection | \"true\", \"false\" on an import file, if the value is at \"true\", new values will be added |  | SingleSelection   | \"true\", \"false\" on an import file, if the value is at \"true\", new values will be added |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_field = new \Swagger\Client\Model\ContactField(); // \Swagger\Client\Model\ContactField | Modèle de ContactField

try {
    $result = $apiInstance->accountPutContactAttribute($contact_field);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountPutContactAttribute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_field** | [**\Swagger\Client\Model\ContactField**](../Model/ContactField.md)| Modèle de ContactField |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountPutContactAttributeValue**
> string accountPutContactAttributeValue($contact_field_value)

Mettre à jour de la valeur du champ en changeant le nom et/ou l'index

##### Informations sur ContactFieldValue #####    | paramètre        | Information / Valeur possible                                                       |  |--------------|------------------------------------------------------------------------------------|  | id           | L'id doit correspondre au champ que vous voulez mettre à jour                            |  | creationDate | La date sera renseignée par défaut avec la date courante            |  | index        | Position où sera enregistrée la valeur, cette nouvelle position doit être vide |   | text         | Le texte qui sera affiché pour cette valeur                                     |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_field_value = new \Swagger\Client\Model\ContactFieldValue(); // \Swagger\Client\Model\ContactFieldValue | Modèle de ContactFieldValue

try {
    $result = $apiInstance->accountPutContactAttributeValue($contact_field_value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountPutContactAttributeValue: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_field_value** | [**\Swagger\Client\Model\ContactFieldValue**](../Model/ContactFieldValue.md)| Modèle de ContactFieldValue |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

