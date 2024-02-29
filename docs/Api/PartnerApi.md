# Swagger\Client\PartnerApi

All URIs are relative to *https://services.message-business.com/api/rest/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**partnerGetPartnerAccount**](PartnerApi.md#partnerGetPartnerAccount) | **GET** /Partner/{mbcode}/{accountId} | Vérifie si un compte partenaire est actif
[**partnerPostPartnerAccount**](PartnerApi.md#partnerPostPartnerAccount) | **POST** /Partner | Créer un nouveau compte Sendethic


# **partnerGetPartnerAccount**
> string partnerGetPartnerAccount($mbcode, $account_id)

Vérifie si un compte partenaire est actif

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$mbcode = "mbcode_example"; // string | Le code fourni par Sendethic
$account_id = 56; // int | account Id

try {
    $result = $apiInstance->partnerGetPartnerAccount($mbcode, $account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnerApi->partnerGetPartnerAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **mbcode** | **string**| Le code fourni par Sendethic |
 **account_id** | **int**| account Id |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **partnerPostPartnerAccount**
> \Swagger\Client\Model\PartnerInformation partnerPostPartnerAccount($partner_signup)

Créer un nouveau compte Sendethic

Cette méthode ne peut être utilisé que par les partenaires de Sendethic. Merci de nous contacter si vous voulez plus d'informations sur le programme partenaire. Un objet vous sera retourné avec les informations du nouveau contact. Si une erreur se produit, l'objet aura une variable erreur décrivant l'erreur.  Un objet vous sera retourné avec les informations du nouveau contact. Si une erreur se produit, l'objet aura une variable erreur décrivant l'erreur    ##### Informations sur PartnerSignUp #####    | paramètre        | Information / Valeur possible                                                |  |--------------|-----------------------------------------------------------------------------|  | mbcode       | Le code fourni par Sendethic                                   |  | salutation   | \"M\", \"Mlle\", \"Mme\"                                                          |  | firstname    | Le prénom de votre client                                               |  | lastname     | Le nom de famille de votre client                                                |  | email        | L'adresse email du premier utilisateur du compte                                    |  | jobtitle     | La fonction ou titre votre client dans son entreprise                                               |  | phonenumber  | Le numéro de téléphone de votre client                                             |  | companyName  | Le nom de l'entreprise de votre client                                             |  | address      | L'adresse de l'entreprise de votre client                                          |  | zipcode      | Le code postal de votre client                                         |  | city         | La ville où se trouve l'entreprise de votre client                                             |  | country      | Le pays où se trouve l'entreprise de votre client                                          |  | culture      | Culture de la langue utilisée, specifiée par deux lettres en minuscules par le code ISO 693-1 suivi par '-' puis deux lettres en majuscule au format ISO 3166 par exemple pour le français de France: \"fr-FR\" |  | website  | The url of your website                 |  | resellerNfo  | Informations supplémentaires si besoin (ex: numéro de licence spécifique)                 |  | sendingEmails  | Définit les adresses utilisées en tant qu’adresses d’envoi dans les opérations    |

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$partner_signup = new \Swagger\Client\Model\PartnerSignUp(); // \Swagger\Client\Model\PartnerSignUp | 

try {
    $result = $apiInstance->partnerPostPartnerAccount($partner_signup);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnerApi->partnerPostPartnerAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **partner_signup** | [**\Swagger\Client\Model\PartnerSignUp**](../Model/PartnerSignUp.md)|  |

### Return type

[**\Swagger\Client\Model\PartnerInformation**](../Model/PartnerInformation.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/xml, text/xml, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

