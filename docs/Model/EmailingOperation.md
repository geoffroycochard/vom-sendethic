# EmailingOperation

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Operation number | [optional] 
**culture** | **string** | Language and localisation ex fr-FR | [optional] 
**status** | **string** | Operation status | [optional] 
**name** | **string** | Operation name | 
**description** | **string** | Description de l&#39;opération | [optional] 
**date** | **string** | Operation start date | [optional] 
**subject** | **string** | Objet du message | 
**from_name** | **string** | Nom d&#39;expéditeur affiché | [optional] 
**from_mail** | **string** | Mail used to send the email | [optional] 
**reply_to** | **string** | L&#39;adresse email ou vous voulez recevoir les réponses | 
**html_editor** | **string** | Message content Html format to be edited in the MB editor | [optional] 
**html** | **string** | Message content Html format | [optional] 
**text** | **string** | Contenu du message au format text | [optional] 
**report_link** | **string** | Url of the report | [optional] 
**receivers** | [**\Swagger\Client\Model\ReceiversOperation**](ReceiversOperation.md) |  | [optional] 
**schedule** | [**\Swagger\Client\Model\ScheduleOperation**](ScheduleOperation.md) |  | [optional] 
**options** | [**\Swagger\Client\Model\EmailingOption**](EmailingOption.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


