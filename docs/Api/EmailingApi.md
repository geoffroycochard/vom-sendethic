# Swagger\Client\EmailingApi

All URIs are relative to *https://services.message-business.com/api/rest/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**emailingApproveEmailingOperation**](EmailingApi.md#emailingApproveEmailingOperation) | **PUT** /emailing/approve/{id} | Valider l&#39;envoi d&#39;une opération
[**emailingDeleteSingleEmailingOperation**](EmailingApi.md#emailingDeleteSingleEmailingOperation) | **DELETE** /emailing/operation/{id} | Supprimer définitivement une opération
[**emailingGetAllEmailingOperation**](EmailingApi.md#emailingGetAllEmailingOperation) | **GET** /emailing/{size} | Obtenir la liste des opérations
[**emailingGetAllExportEmailingOperation**](EmailingApi.md#emailingGetAllExportEmailingOperation) | **GET** /emailing/exports/{size} | Obtenir la liste de tous les exports d&#39;activités sur les destinataires d&#39;opérations
[**emailingGetExportEmailingOperation**](EmailingApi.md#emailingGetExportEmailingOperation) | **GET** /emailing/export/{id} | Obtenir les informations d&#39;un export d&#39;activités sur les destinataires d&#39;une opération
[**emailingGetFileExport**](EmailingApi.md#emailingGetFileExport) | **GET** /emailing/export/file/{fileName} | Télécharger le fichier d&#39;archive de l&#39;export
[**emailingGetSingleEmailingOperation**](EmailingApi.md#emailingGetSingleEmailingOperation) | **GET** /emailing/operation/{id} | Obtenir les informations d&#39;une opération
[**emailingGetStatusEmailingOperation**](EmailingApi.md#emailingGetStatusEmailingOperation) | **GET** /emailing/status/{status}/{size} | Obtenir les opérations par status
[**emailingPostEmailingOperation**](EmailingApi.md#emailingPostEmailingOperation) | **POST** /emailing | Créer une opération
[**emailingPostExportEmailingOperation**](EmailingApi.md#emailingPostExportEmailingOperation) | **POST** /emailing/export/add/{id} | Ajouter un export d&#39;activités sur les destinataires d&#39;une opération spécifique
[**emailingPostSendSmtp**](EmailingApi.md#emailingPostSendSmtp) | **POST** /emailing/sendsmtp/{id} | Faire un envoi SMTP Transactionnel en reprenant le contenu HTML et TEXT d&#39;une opération spécifique
[**emailingPostTestOperation**](EmailingApi.md#emailingPostTestOperation) | **POST** /emailing/test/{id} | Envoyer un email de test
[**emailingPutEmailingOperation**](EmailingApi.md#emailingPutEmailingOperation) | **PUT** /emailing | Mettre à jour une opération
[**emailingResumeEmailingOperation**](EmailingApi.md#emailingResumeEmailingOperation) | **PUT** /emailing/resume/{id} | Reprendre une opération
[**emailingSearchEmailingOperation**](EmailingApi.md#emailingSearchEmailingOperation) | **POST** /emailing/search/{size} | Recherche d&#39;une opération en fonction des paramètres
[**emailingSuspendEmailingOperation**](EmailingApi.md#emailingSuspendEmailingOperation) | **PUT** /emailing/suspend/{id} | Suspendre une opération


# **emailingApproveEmailingOperation**
> string emailingApproveEmailingOperation($id)

Valider l'envoi d'une opération

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id de l'opération d'emailing

try {
    $result = $apiInstance->emailingApproveEmailingOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingApproveEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id de l&#39;opération d&#39;emailing |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingDeleteSingleEmailingOperation**
> \Swagger\Client\Model\EmailingOperation emailingDeleteSingleEmailingOperation($id)

Supprimer définitivement une opération

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 

try {
    $result = $apiInstance->emailingDeleteSingleEmailingOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingDeleteSingleEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  |

### Return type

[**\Swagger\Client\Model\EmailingOperation**](../Model/EmailingOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingGetAllEmailingOperation**
> \Swagger\Client\Model\EmailingOperation[] emailingGetAllEmailingOperation($size)

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


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$size = 56; // int | Le nombre d'opération à afficher, 50 par défaut et 500 maximum

try {
    $result = $apiInstance->emailingGetAllEmailingOperation($size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingGetAllEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **size** | **int**| Le nombre d&#39;opération à afficher, 50 par défaut et 500 maximum |

### Return type

[**\Swagger\Client\Model\EmailingOperation[]**](../Model/EmailingOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingGetAllExportEmailingOperation**
> \Swagger\Client\Model\EmailingOperationExport[] emailingGetAllExportEmailingOperation($size)

Obtenir la liste de tous les exports d'activités sur les destinataires d'opérations

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$size = 56; // int | Le nombre d'opération à afficher, 50 par défaut et 500 maximum

try {
    $result = $apiInstance->emailingGetAllExportEmailingOperation($size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingGetAllExportEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **size** | **int**| Le nombre d&#39;opération à afficher, 50 par défaut et 500 maximum |

### Return type

[**\Swagger\Client\Model\EmailingOperationExport[]**](../Model/EmailingOperationExport.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingGetExportEmailingOperation**
> \Swagger\Client\Model\EmailingOperationExport emailingGetExportEmailingOperation($id)

Obtenir les informations d'un export d'activités sur les destinataires d'une opération



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id de l'export d'activité emailing

try {
    $result = $apiInstance->emailingGetExportEmailingOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingGetExportEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id de l&#39;export d&#39;activité emailing |

### Return type

[**\Swagger\Client\Model\EmailingOperationExport**](../Model/EmailingOperationExport.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingGetFileExport**
> emailingGetFileExport($file_name)

Télécharger le fichier d'archive de l'export

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file_name = "file_name_example"; // string | Nom du fichier d'archive

try {
    $apiInstance->emailingGetFileExport($file_name);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingGetFileExport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_name** | **string**| Nom du fichier d&#39;archive |

### Return type

void (empty response body)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingGetSingleEmailingOperation**
> \Swagger\Client\Model\EmailingOperation emailingGetSingleEmailingOperation($id)

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


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | L'id de l'emailing

try {
    $result = $apiInstance->emailingGetSingleEmailingOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingGetSingleEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| L&#39;id de l&#39;emailing |

### Return type

[**\Swagger\Client\Model\EmailingOperation**](../Model/EmailingOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingGetStatusEmailingOperation**
> \Swagger\Client\Model\EmailingOperation[] emailingGetStatusEmailingOperation($status, $size)

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


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = "status_example"; // string | Le status de l'opération
$size = 56; // int | Le nombre d'opération à afficher, 50 par défaut et 500 maximum

try {
    $result = $apiInstance->emailingGetStatusEmailingOperation($status, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingGetStatusEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **string**| Le status de l&#39;opération |
 **size** | **int**| Le nombre d&#39;opération à afficher, 50 par défaut et 500 maximum |

### Return type

[**\Swagger\Client\Model\EmailingOperation[]**](../Model/EmailingOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingPostEmailingOperation**
> \Swagger\Client\Model\EmailingOperation emailingPostEmailingOperation($email_op)

Créer une opération

Ceci créera une opération, chaque valeur non-renseignée aura par défaut la valeur configurée sur le compte   Pour valider l'envoi d'une opération, vous devrez faire un appel de type PUT car ce type d'opération est effectué de manière asynchrone.  Les valeurs **name**, **subject** et **replyTo** sont obligatoires.  #### EmailingOperation notes ####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | Cette valeur sera ignorée                         |  | status       | Cette valeur sera ignorée (read only)             |  | culture      | \"en-us\", \"es-es\", \"pt-pt\", \"it-it\", \"de-de\", \"nl-nl\", \"zh-cn\", \"zh-ht\", \"fr-fr\" |  | name         | Le nom de l'opération avec un maximum de 256 caractères    |  | description  | Description de l'opération                              |  | date         | La date de début de l'opération au format UTC \"yyyy-MM-dd HH:mm:ss+0000\", Toujours mettre le +0000 afin que la periode s'affiche bien au format UTC. Dépend du type de la classe schedule |  | subject      | Objet du message                                      |  | fromName     | Nom d'expéditeur affiché                       |  | fromMail     | Adresse email d'envoi (doit être préalablement paramétré dans Votre compte > Paramètres > Emailings) |  | replyTo      | L'adresse email ou vous voulez recevoir les réponses |  | htmlEditor   | Contenu du message au format html à editer dans L'Editeur du compte Sendethic avant envoi (option - uniquement si le contenu doit être édité dans L'Editeur par un utilisateur du compte Sendethic) |  | html         | Contenu du message au format html à envoyer                         |  | text         | Contenu du message au format text                     |  | receivers    | Sélection des destinataires, voir ci-dessous pour plus de détails      |  | schedule     | Planning d'envoi d'une opération, voir ci-dessous pour plus de details |  | options      | Options avancées, voir ci-dessous pour plus de détails            |    #### EmailingOption notes ####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | mirror             | \"false\", \"account\", \"true\"                         |  | mirrorParagraph    | Contenu au format html repris si la valeur mirror est positionnée à true                 |  | encoding           | \"utf-8\", \"iso-8859-15\", \"utf-7\", \"us-ascii\", \"iso-8859-6\", \"windows-1256\", \"iso-8859-4\", \"windows-1257\", \"iso-8859-2\", \"windows-1250\", \"gb2312\", \"hz-gb-2312\", \"GB18030\", \"Big5\", \"iso-8859-5\", \"windows-1251\", \"koi8-r\", \"koi8-u\", \"iso-8859-7\", \"iso-8859-8-i\", \"windows-1255\", \"euc-jp\", \"iso-2022-jp\", \"csISO2022JP\", \"shift_jis\", \"euc-kr\", \"iso-2022-kr\", \"ks_c_5601-1987\", \"iso-8859-3\", \"windows-874\", \"iso-8859-9\", \"windows-1254\", \"windows-1258\", \"iso-8859-1\", \"windows-1252\"  |  | importance         | \"normal\", \"low\", \"high\"                |  | contentFormat      | \"html\", \"text\", vous pouvez utiliser la variable text aussi si vous choisissez le html   |  | recipientDisplay   | Format d'affichage de l'adresse des destinataires : \"`**`mb_email`**`\", \"`**`mb_firstname`**` `**`mb_lastname`**`\", \"`**`mb_lastname`**` `**`mb_firstname`**`\", \"`**`mb_firstname`**`\" ou your own value |  | redirectBounce     | Renseignez l'adresse email sur laquelle rediriger les retours serveur (bounce)         |  | redirectValidation | Renseignez l'adresse email sur laquelle rediriger les spam-challenge                                   |  | routingOption      | Rediriger l'envoi vers une adresse d'un champs personnalisé ou une adresse email que celui du destinataire                                   |  | analyticsOption    | \"no\", \"xiti\", \"google\",   |  | xitiPrefix         | Préfixe des URLs sur lesquels utiliser les paramètres Xiti       |  | xitiTag            | Xiti tag                                   |  | gaSource           | google analytics utm_source                                 |  | gaMedium           | google analytics utm_medium                                 |  | gaCampaign         | google analytics utm_campaign                               |  | gaContent          | google analytics utm_content                                |  | gaTerm             | google analytics utm_Term                                   |  | gaPrefix           | Préfixe des URLs sur lesquels utiliser les paramètres Google Analytics          |    #### Détail de ReceiversOperation ####    | paramètre         | Information / Valeur possible                          |  |---------------|-------------------------------------------------------|  | segmentIds    | Liste d'id de segment                                   |  | importIds     | Liste d'id d'import                                    |  | contactIds    | Liste d'id de contact                                   |  | conditionsXml | Format XML                                          |    #### Détails de ScheduleOperation ####    Assurez-vous de renseigner le type pour que la mise à jour soit enregistrée    | paramètre        | Information / Valeur possible                               |  |--------------|------------------------------------------------------------|  | type           | \"asap\", \"triggered\", \"scheduled\". La classe Scheduled est dependant de la variable date de EmailingOperation  |  | criterias      | Les critères au format XML                              |  | criteriasMode  | \"intersect\", \"union\", la valeur par défault est intersect                                      |  | criteriasTime  | Le temps qui s'écoulera entre l'atteinte des critères et le début de l'envoi de l'operation, vous avez la possibilité de choisir le temps en heure, jour, semaine ou mois comme ceci h[0-24], d[1-14], w[2-3], m[1-3]. Par exemple \"h0\" enverra quelques minutes apres l'atteinte des critères, \"h3\" 3 heures après, \"w2\" 2 semaines après  |  | criteriasLimit | Limiter à un seul envoi de l'opération par destinataire, \"true\", \"false\" |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email_op = new \Swagger\Client\Model\EmailingOperation(); // \Swagger\Client\Model\EmailingOperation | 

try {
    $result = $apiInstance->emailingPostEmailingOperation($email_op);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingPostEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_op** | [**\Swagger\Client\Model\EmailingOperation**](../Model/EmailingOperation.md)|  |

### Return type

[**\Swagger\Client\Model\EmailingOperation**](../Model/EmailingOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingPostExportEmailingOperation**
> \Swagger\Client\Model\EmailingOperationExport emailingPostExportEmailingOperation($id, $export_nfo)

Ajouter un export d'activités sur les destinataires d'une opération spécifique

#### EmailingOperationExport notes ####    | paramètre        | Information / Valeur possible                                       |  |--------------|--------------------------------------------------------------------|  | startDate     | Date de début. Cette valeur doit être au format de date UTC \"yyyy-MM-dd HH:mm:ss\" |  | endDate       | Date de fin. Cette valeur doit être au format de date UTC \"yyyy-MM-dd HH:mm:ss\" |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id de l'opération d'emailing
$export_nfo = new \Swagger\Client\Model\EmailingOperationExport(); // \Swagger\Client\Model\EmailingOperationExport | 

try {
    $result = $apiInstance->emailingPostExportEmailingOperation($id, $export_nfo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingPostExportEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id de l&#39;opération d&#39;emailing |
 **export_nfo** | [**\Swagger\Client\Model\EmailingOperationExport**](../Model/EmailingOperationExport.md)|  |

### Return type

[**\Swagger\Client\Model\EmailingOperationExport**](../Model/EmailingOperationExport.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingPostSendSmtp**
> string emailingPostSendSmtp($id, $smtp_email)

Faire un envoi SMTP Transactionnel en reprenant le contenu HTML et TEXT d'une opération spécifique

#### SmtpEmail notes ####    | paramètre        | Information / Valeur possible                                       |  |--------------|--------------------------------------------------------------------|  | recipientEmail     | Adresse email du destinataire |  | recipientName       | Nom du destinataire |  | recipientDatas     | Tableau des données de personnalisation sous forme de liste \"id\" : \"valeur\"

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id de l'opération d'emailing
$smtp_email = new \Swagger\Client\Model\SmtpEmail(); // \Swagger\Client\Model\SmtpEmail | 

try {
    $result = $apiInstance->emailingPostSendSmtp($id, $smtp_email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingPostSendSmtp: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id de l&#39;opération d&#39;emailing |
 **smtp_email** | [**\Swagger\Client\Model\SmtpEmail**](../Model/SmtpEmail.md)|  |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingPostTestOperation**
> string emailingPostTestOperation($id, $email_test)

Envoyer un email de test

#### Informations sur TestEmail ####    | paramètre        | Information / Valeur possible                                       |  |--------------|--------------------------------------------------------------------|  | recipientUser           | email de l'utilisateur destinataire (to)                |  | testContact       | email du contact utilisé pour la personnalisation de l'envoi de test      |  | titlePrefix      | prefixe de l'objet |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id de l'opération d'emailing
$email_test = new \Swagger\Client\Model\TestEmail(); // \Swagger\Client\Model\TestEmail | 

try {
    $result = $apiInstance->emailingPostTestOperation($id, $email_test);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingPostTestOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id de l&#39;opération d&#39;emailing |
 **email_test** | [**\Swagger\Client\Model\TestEmail**](../Model/TestEmail.md)|  |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingPutEmailingOperation**
> string emailingPutEmailingOperation($email_op)

Mettre à jour une opération

Ceci vous permet de mettre à jour les paramétres d'une opération d'emailing, si vous laissez une valeur à null celui-ci sera ignorée.  #### EmailingOperation notes ####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | id           | L'id qui identifie l'opération a modifier     |  | status       | Cette valeur sera ignorée (read only)             |  | culture      | \"en-us\", \"es-es\", \"pt-pt\", \"it-it\", \"de-de\", \"nl-nl\", \"zh-cn\", \"zh-ht\", \"fr-fr\" |  | name         | Le nom de l'opération avec un maximum de 256 caractères    |  | description  | Description de l'opération                              |  | date         | La date de début de l'opération au format UTC \"yyyy-MM-dd HH:mm:ss +0000\", Toujours mettre le +0000 afin que la periode s'affiche bien au format UTC. Dépend du type de la classe schedule |  | subject      | Objet du message                                      |  | fromName     | Nom d'expéditeur affiché                       |  | fromMail     | Mail used to send the email (must be defined in your account parameters)      |  | replyTo      | L'adresse email ou vous voulez recevoir les réponses |  | htmlEditor   | Contenu du message au format html à editer dans L'Editeur du compte Sendethic avant envoi (option - uniquement si le contenu doit être édité dans L'Editeur par un utilisateur du compte Sendethic) |  | html         | Contenu du message au format html à envoyer                         |  | text         | Contenu du message au format text                     |  | receivers    | Sélection des destinataires, voir ci-dessous pour plus de détails      |  | schedule     | Planning d'envoi d'une opération, voir ci-dessous pour plus de details |  | options      | Options avancées, voir ci-dessous pour plus de détails            |    #### EmailingOption notes ####    | paramètre        | Information / Valeur possible                                                  |  |--------------|-------------------------------------------------------------------------------|  | mirror             | \"false\", \"account\", \"true\"                         |  | mirrorParagraph    | Contenu au format html repris si la valeur mirror est positionnée à true                 |  | encoding           | \"utf-8\", \"iso-8859-15\", \"utf-7\", \"us-ascii\", \"iso-8859-6\", \"windows-1256\", \"iso-8859-4\", \"windows-1257\", \"iso-8859-2\", \"windows-1250\", \"gb2312\", \"hz-gb-2312\", \"GB18030\", \"Big5\", \"iso-8859-5\", \"windows-1251\", \"koi8-r\", \"koi8-u\", \"iso-8859-7\", \"iso-8859-8-i\", \"windows-1255\", \"euc-jp\", \"iso-2022-jp\", \"csISO2022JP\", \"shift_jis\", \"euc-kr\", \"iso-2022-kr\", \"ks_c_5601-1987\", \"iso-8859-3\", \"windows-874\", \"iso-8859-9\", \"windows-1254\", \"windows-1258\", \"iso-8859-1\", \"windows-1252\"  |  | importance         | \"normal\", \"low\", \"high\"                |  | contentFormat      | \"html\", \"text\", vous pouvez utiliser la variable text aussi si vous choisissez le html   |  | recipientDisplay   | Format d'affichage de l'adresse des destinataires : \"`**`mb_email`**`\", \"`**`mb_firstname`**` `**`mb_lastname`**`\", \"`**`mb_lastname`**` `**`mb_firstname`**`\", \"`**`mb_firstname`**`\" ou your own value |  | redirectBounce     | Renseignez l'adresse email sur laquelle rediriger les retours serveur (bounce)         |  | redirectValidation | Renseignez l'adresse email sur laquelle rediriger les spam-challenge                                   |  | routingOption      | Rediriger l'envoi vers une adresse d'un champs personnalisé ou une adresse email que celui du destinataire                                   |  | analyticsOption    | \"no\", \"xiti\", \"google\",   |  | xitiPrefix         | Préfixe des URLs sur lesquels utiliser les paramètres Xiti       |  | xitiTag            | Xiti tag                                   |  | gaSource           | google analytics utm_source                                 |  | gaMedium           | google analytics utm_medium                                 |  | gaCampaign         | google analytics utm_campaign                               |  | gaContent          | google analytics utm_content                                |  | gaTerm             | google analytics utm_Term                                   |  | gaPrefix           | Préfixe des URLs sur lesquels utiliser les paramètres Google Analytics          |    #### Détail de ReceiversOperation ####    | paramètre         | Information / Valeur possible                          |  |---------------|-------------------------------------------------------|  | segmentIds    | Liste d'id de segment                                   |  | importIds     | Liste d'id d'import                                    |  | contactIds    | Liste d'id de contact                                   |  | conditionsXml | Format XML                                          |    #### Détails de ScheduleOperation ####    | paramètre        | Information / Valeur possible                               |  |--------------|------------------------------------------------------------|  | type           | \"asap\", \"triggered\", \"scheduled\". La classe Scheduled est dependant de la variable date de EmailingOperation  |  | criterias      | Les critères au format XML                              |  | criteriasMode  | \"intersect\", \"union\", the la valeur par défault est intersect  |  | criteriasTime  | Le temps qui s'écoulera entre l'atteinte des critères et le début de l'envoi de l'operation, vous avez la possibilité de choisir le temps en heure, jour, semaine ou mois comme ceci h[0-24], d[1-14], w[2-3], m[1-3]. Par exemple \"h0\" enverra quelques minutes apres l'atteinte des critères, \"h3\" 3 heures après, \"w2\" 2 semaines après  |  | criteriasLimit | Limiter à un seul envoi de l'opération par destinataire, \"true\", \"false\" |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email_op = new \Swagger\Client\Model\EmailingOperation(); // \Swagger\Client\Model\EmailingOperation | 

try {
    $result = $apiInstance->emailingPutEmailingOperation($email_op);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingPutEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_op** | [**\Swagger\Client\Model\EmailingOperation**](../Model/EmailingOperation.md)|  |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingResumeEmailingOperation**
> string emailingResumeEmailingOperation($id)

Reprendre une opération

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id de l'opération d'emailing

try {
    $result = $apiInstance->emailingResumeEmailingOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingResumeEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id de l&#39;opération d&#39;emailing |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingSearchEmailingOperation**
> \Swagger\Client\Model\EmailingOperation[] emailingSearchEmailingOperation($search, $size)

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


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$search = new \Swagger\Client\Model\SearchOperation(); // \Swagger\Client\Model\SearchOperation | l'objet de recherche
$size = 56; // int | Le nombre d'opération à afficher, 50 par défaut et 500 maximum

try {
    $result = $apiInstance->emailingSearchEmailingOperation($search, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingSearchEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search** | [**\Swagger\Client\Model\SearchOperation**](../Model/SearchOperation.md)| l&#39;objet de recherche |
 **size** | **int**| Le nombre d&#39;opération à afficher, 50 par défaut et 500 maximum |

### Return type

[**\Swagger\Client\Model\EmailingOperation[]**](../Model/EmailingOperation.md)

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **emailingSuspendEmailingOperation**
> string emailingSuspendEmailingOperation($id)

Suspendre une opération

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: basic
$config = Swagger\Client\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Swagger\Client\Api\EmailingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | id de l'opération d'emailing

try {
    $result = $apiInstance->emailingSuspendEmailingOperation($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailingApi->emailingSuspendEmailingOperation: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| id de l&#39;opération d&#39;emailing |

### Return type

**string**

### Authorization

[basic](../../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

