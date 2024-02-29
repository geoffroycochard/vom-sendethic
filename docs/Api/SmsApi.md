# Swagger\Client\SmsApi

All URIs are relative to *https://services.message-business.com/api/rest/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**smsApproveSmsOperation**](SmsApi.md#smsApproveSmsOperation) | **PUT** /sms/approve/{id} | Valider l&#39;envoi d&#39;une opération
[**smsDeleteSingleSmsOperation**](SmsApi.md#smsDeleteSingleSmsOperation) | **DELETE** /sms/operation/{id} | Supprimer définitivement une opération
[**smsGetAllSmsOperation**](SmsApi.md#smsGetAllSmsOperation) | **GET** /sms/{size} | Obtenir la liste des opérations
[**smsGetSingleSmsOperation**](SmsApi.md#smsGetSingleSmsOperation) | **GET** /sms/operation/{id} | Obtenir les informations d&#39;une opération
[**smsGetStatusSmsOperation**](SmsApi.md#smsGetStatusSmsOperation) | **GET** /sms/status/{status}/{size} | Obtenir les opérations par status
[**smsPostSmsOperation**](SmsApi.md#smsPostSmsOperation) | **POST** /sms | Créer une opération
[**smsPutSmsOperation**](SmsApi.md#smsPutSmsOperation) | **PUT** /sms | Mettre à jour une opération
[**smsResumeSmsOperation**](SmsApi.md#smsResumeSmsOperation) | **PUT** /sms/resume/{id} | Reprendre une opération
[**smsSearchEmailingOperation**](SmsApi.md#smsSearchEmailingOperation) | **POST** /sms/search/{size} | Recherche d&#39;une opération en fonction des paramètres
[**smsSendSms**](SmsApi.md#smsSendSms) | **POST** /sms/send | Envoyer un sms
[**smsSuspendSmsOperation**](SmsApi.md#smsSuspendSmsOperation) | **PUT** /sms/suspend/{id} | Suspendre une opération


# **smsApproveSmsOperation**
> string smsApproveSmsOperation($id)

Valider l'envoi d'une opération

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Id de l'opération sms

try {
    $result = $apiInstance->smsApproveSmsOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsApproveSmsOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Id de l&#39;opération sms |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsDeleteSingleSmsOperation**
> \Swagger\Client\Model\SmsOperation smsDeleteSingleSmsOperation($id)

Supprimer définitivement une opération

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 

try {
    $result = $apiInstance->smsDeleteSingleSmsOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsDeleteSingleSmsOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  |

### Return type

[**\Swagger\Client\Model\SmsOperation**](../Model/SmsOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsGetAllSmsOperation**
> \Swagger\Client\Model\SmsOperation[] smsGetAllSmsOperation($size)

Obtenir la liste des opérations

La classe receiver et schedule seront toujours null, utilisez l'appel d'opération avec son id pour obtenir plus d'informations

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$size = 56; // int | Le nombre d'opération à afficher, 50 par défaut et 500 maximum

try {
    $result = $apiInstance->smsGetAllSmsOperation($size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsGetAllSmsOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **size** | **int**| Le nombre d&#39;opération à afficher, 50 par défaut et 500 maximum |

### Return type

[**\Swagger\Client\Model\SmsOperation[]**](../Model/SmsOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsGetSingleSmsOperation**
> \Swagger\Client\Model\SmsOperation smsGetSingleSmsOperation($id)

Obtenir les informations d'une opération

- L'objet receiver vous donnera une liste d'id pour chaque ressource respective  - L'objet schedule vous donnera une liste d'id pour chaque ressource respective    #### Schedule type ####    | type | variable and explanation |  |------|--------------------------|  | \"asap\" | Ce type fera partir l'operation dès que possible |  | \"scheduled\" | Ce type fera partir l'operation à la date que vous trouverez dans la variable **data** |  | \"triggered\" | Ce type fera partir l'opération dès que les critères renseignés dans la variable **criterias** seront atteint. Cette variable sera à remplir au format xml. C'est le même format utilisé dans les segments. |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | L'id de l'opération de sms

try {
    $result = $apiInstance->smsGetSingleSmsOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsGetSingleSmsOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| L&#39;id de l&#39;opération de sms |

### Return type

[**\Swagger\Client\Model\SmsOperation**](../Model/SmsOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsGetStatusSmsOperation**
> \Swagger\Client\Model\SmsOperation[] smsGetStatusSmsOperation($status, $size)

Obtenir les opérations par status

| Status possible values |  |-----------------------------------------------|  | \"edited\", \"running\", \"completed\", \"suspended\" |  La classe receiver et schedule seront toujours null, utilisez l'appel d'opération avec son id pour obtenir plus d'informations

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = "status_example"; // string | Le status de l'opération
$size = 56; // int | Le nombre d'opération à afficher, 50 par défaut et 500 maximum

try {
    $result = $apiInstance->smsGetStatusSmsOperation($status, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsGetStatusSmsOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **string**| Le status de l&#39;opération |
 **size** | **int**| Le nombre d&#39;opération à afficher, 50 par défaut et 500 maximum |

### Return type

[**\Swagger\Client\Model\SmsOperation[]**](../Model/SmsOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsPostSmsOperation**
> \Swagger\Client\Model\SmsOperation smsPostSmsOperation($sms_op)

Créer une opération

Ceci créera une opération, chaque valeur non-renseignée aura par défaut la valeur configurée sur le compte   Pour valider l'envoi d'une opération, vous devrez faire un appel de type PUT car ce type d'opération est effectué de manière asynchrone.  La valeur **name** est obligatoire.  #### SmsOperation notes ####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | Cette valeur sera ignorée                         |  | status       | Cette valeur sera ignorée (read only)             |  | name         | Le nom de l'opération avec un maximum de 256 caractères    |  | description  | Description de l'opération                              |  | date         | La date de début de l'opération au format UTC \"yyyy-MM-dd HH:mm:ss+0000\", Toujours mettre le +0000 afin que la periode s'affiche bien au format UTC. Dépend du type de la classe schedule |  | oadc         | Si vous souhaitez personnaliser le nom de l'émetteur (optionnel)                                      |  | message      | Le message que vous souhaitez envoyer                       |  | receivers    | Sélection des destinataires, voir ci-dessous pour plus de détails      |  | schedule     | Planning d'envoi d'une opération, voir ci-dessous pour plus de details |    #### Détail de ReceiversOperation ####    | paramètre         | Information / Valeur possible                          |  |---------------|-------------------------------------------------------|  | segmentIds    | Liste d'id de segment                                   |  | importIds     | Liste d'id d'import                                    |  | contactIds    | Liste d'id de contact                                   |  | conditionsXml | Format XML                                          |    #### Détails de ScheduleOperation ####    Assurez-vous de renseigner le type pour que la mise à jour soit enregistrée    | paramètre        | Information / Valeur possible                               |  |--------------|------------------------------------------------------------|  | type           | \"asap\", \"triggered\", \"scheduled\". Scheduled is dependent on the SmsOption date and triggered on the variables below  |  | criterias      | Les critères au format XML                              |  | criteriasMode  | \"intersect\", \"union\", la valeur par défault est intersect                                      |  | criteriasTime  | Le temps qui s'écoulera entre l'atteinte des critères et le début de l'envoi de l'operation, vous avez la possibilité de choisir le temps en heure, jour, semaine ou mois comme ceci h[0-24], d[1-14], w[2-3], m[1-3]. Par exemple \"h0\" enverra quelques minutes apres l'atteinte des critères, \"h3\" 3 heures après, \"w2\" 2 semaines après  |  | criteriasLimit | Limit to one operation per recipient, \"true\", \"false\" |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_op = new \Swagger\Client\Model\SmsOperation(); // \Swagger\Client\Model\SmsOperation | 

try {
    $result = $apiInstance->smsPostSmsOperation($sms_op);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsPostSmsOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_op** | [**\Swagger\Client\Model\SmsOperation**](../Model/SmsOperation.md)|  |

### Return type

[**\Swagger\Client\Model\SmsOperation**](../Model/SmsOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsPutSmsOperation**
> string smsPutSmsOperation($sms_op)

Mettre à jour une opération

Ceci vous permet de mettre à jour les paramétres d'une opération d'emailing, si vous laissez une valeur à null celui-ci sera ignorée.  #### SmsOperation notes ####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | L'id qui identifie l'opération a modifier     |  | status       | Cette valeur sera ignorée (read only)             |  | name         | Le nom de l'opération avec un maximum de 256 caractères    |  | description  | Description de l'opération                              |  | date         | La date de début de l'opération au format UTC \"yyyy-MM-dd HH:mm:ss+0000\", Toujours mettre le +0000 afin que la periode s'affiche bien au format UTC. Dépend du type de la classe schedule |  | oadc         | Si vous souhaitez personnaliser le nom de l'émetteur (optionnel)                                      |  | message      | Le message que vous souhaitez envoyer                       |  | receivers    | Sélection des destinataires, voir ci-dessous pour plus de détails      |  | schedule     | Planning d'envoi d'une opération, voir ci-dessous pour plus de details |    #### Détail de ReceiversOperation ####    | paramètre         | Information / Valeur possible                          |  |---------------|-------------------------------------------------------|  | segmentIds    | Liste d'id de segment                                   |  | importIds     | Liste d'id d'import                                    |  | contactIds    | Liste d'id de contact                                   |  | conditionsXml | Format XML                                          |    #### Détails de ScheduleOperation ####    | paramètre        | Information / Valeur possible                               |  |--------------|------------------------------------------------------------|  | type           | \"asap\", \"triggered\", \"scheduled\". Scheduled is dependent on the SmsOption date and triggered on the variables below  |  | criterias      | Les critères au format XML                              |  | criteriasMode  | \"intersect\", \"union\", the la valeur par défault est intersect  |  | criteriasTime  | Le temps qui s'écoulera entre l'atteinte des critères et le début de l'envoi de l'operation, vous avez la possibilité de choisir le temps en heure, jour, semaine ou mois comme ceci h[0-24], d[1-14], w[2-3], m[1-3]. Par exemple \"h0\" enverra quelques minutes apres l'atteinte des critères, \"h3\" 3 heures après, \"w2\" 2 semaines après  |  | criteriasLimit | Limit to one operation per recipient, \"true\", \"false\" |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_op = new \Swagger\Client\Model\SmsOperation(); // \Swagger\Client\Model\SmsOperation | 

try {
    $result = $apiInstance->smsPutSmsOperation($sms_op);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsPutSmsOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_op** | [**\Swagger\Client\Model\SmsOperation**](../Model/SmsOperation.md)|  |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsResumeSmsOperation**
> string smsResumeSmsOperation($id)

Reprendre une opération

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Id de l'opération sms

try {
    $result = $apiInstance->smsResumeSmsOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsResumeSmsOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Id de l&#39;opération sms |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsSearchEmailingOperation**
> \Swagger\Client\Model\SmsOperation[] smsSearchEmailingOperation($search, $size)

Recherche d'une opération en fonction des paramètres

#### Informations sur SearchOperation ####    | paramètre        | Information / Valeur possible   |  |------|--------------------------|  | importIds | liste d'ids |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$search = new \Swagger\Client\Model\SearchOperation(); // \Swagger\Client\Model\SearchOperation | l'objet de recherche
$size = 56; // int | Le nombre d'opération à afficher, 50 par défaut et 500 maximum

try {
    $result = $apiInstance->smsSearchEmailingOperation($search, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsSearchEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search** | [**\Swagger\Client\Model\SearchOperation**](../Model/SearchOperation.md)| l&#39;objet de recherche |
 **size** | **int**| Le nombre d&#39;opération à afficher, 50 par défaut et 500 maximum |

### Return type

[**\Swagger\Client\Model\SmsOperation[]**](../Model/SmsOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsSendSms**
> string smsSendSms($sms)

Envoyer un sms

Cette méthode vous permet d'envoyer un SMS à un contact en spécifiant son numéro - Assurez-vous que vous disposez d'assez de crédit d'envoi avant de procéder.  #### Informations sur SmsMessage ####    | paramètre     | Information / Valeur possible                                                  |  |-----------|-------------------------------------------------------------------------------|  | oadc      | Si vous souhaitez personnaliser le nom de l'émetteur (optionnel)                         |  | mobile    | Le numéro de portable sur lequel vous souhaitez envoyer votre message, utiliser le format international (ex pour la france +33612340001) |  | message   | Le message que vous souhaitez envoyer |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms = new \Swagger\Client\Model\SmsMessage(); // \Swagger\Client\Model\SmsMessage | 

try {
    $result = $apiInstance->smsSendSms($sms);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsSendSms: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms** | [**\Swagger\Client\Model\SmsMessage**](../Model/SmsMessage.md)|  |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsSuspendSmsOperation**
> string smsSuspendSmsOperation($id)

Suspendre une opération

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Id de l'opération sms

try {
    $result = $apiInstance->smsSuspendSmsOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsSuspendSmsOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Id de l&#39;opération sms |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

