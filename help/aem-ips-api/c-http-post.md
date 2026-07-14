---
title: Chargement de ressources au moyen de POST HTTP vers le servlet UploadFile
description: Le chargement de ressources dans  [!DNL Dynamic Media]  Classic implique une ou plusieurs requêtes HTTP POST qui configurent une tâche pour coordonner toute l’activité de journal associée aux fichiers chargés.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
TQID: 'https://experienceleague.adobe.com/-sHJjbnmxKSlU8TiOx96f1fgRUVWElHZ6KAqhy0HW0c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 716
ht-degree: 2%

---

# Chargement de ressources au moyen de POST HTTP vers le servlet UploadFile{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Le chargement de ressources dans Dynamic Media Classic implique une ou plusieurs requêtes HTTP POST qui configurent une tâche pour coordonner toute l’activité de journal associée aux fichiers chargés.

Utilisez l’URL suivante pour accéder au servlet UploadFile :

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Toutes les requêtes POST pour une tâche de chargement doivent provenir de la même adresse IP.

**URL d’accès aux régions Dynamic Media**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Localisation géographique </p> </th> 
   <th colname="col2" class="entry"> <p>URL de production </p> </th> 
   <th colname="col3" class="entry"> <p>URL d’évaluation (à utiliser pour le développement et les tests de pré-production) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Amérique du Nord </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europe, Moyen-Orient, Asie </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japon/Asie-Pacifique </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## Workflow de la tâche de chargement {#section-873625b9512f477c992f5cdd77267094}

La tâche de chargement se compose d’une ou de plusieurs requêtes HTTP POST qui utilisent une `jobHandle` commune pour mettre en corrélation le traitement dans la même tâche. Chaque requête est codée en `multipart/form-data` et se compose des parties de formulaire suivantes :

>[!NOTE]
>
>Toutes les requêtes POST pour une tâche de chargement doivent provenir de la même adresse IP.

|  Partie de formulaire HTTP POST  |  Description  |
|---|---|
| `auth`  |   Obligatoire. Un document authHeader XML spécifiant l’authentification et les informations du client. Voir **Demander l’authentification** sous [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Facultatif. Vous pouvez inclure un ou plusieurs fichiers à charger avec chaque requête POST. Chaque partie de fichier peut inclure un paramètre de nom de fichier dans l’en-tête Content-Disposition utilisé comme nom de fichier cible dans IPS si aucun paramètre de `uploadPostParams/fileName` n’est spécifié. |

|  Partie de formulaire HTTP POST   |  Nom de l’élément uploadPostParams   |  Type   |  Description   |
|---|---|---|---|
| `uploadParams` (obligatoire). Un document `uploadParams` XML spécifiant les paramètres de chargement)   |   `companyHandle`  |  `xsd:string`  | Obligatoire. Gérer vers la société vers laquelle le fichier est en cours de chargement. |
| `uploadParams` (obligatoire). Un document `uploadParams` XML spécifiant les paramètres de chargement) | `jobName`  |  `xsd:string`  | Vous devez indiquer `jobName` ou `jobHandle`. Nom de la tâche de chargement. |
| `uploadParams` (obligatoire). Un document `uploadParams` XML spécifiant les paramètres de chargement) | `jobHandle`  |  `xsd:string`  | Vous devez indiquer `jobName` ou `jobHandle`. Gérer vers une tâche de chargement démarrée dans une requête précédente. |
| `uploadParams` (obligatoire). Un document `uploadParams` XML spécifiant les paramètres de chargement) | `locale`  |  `xsd:string`  | Facultatif. Code de langue et de pays pour la localisation. |
| `uploadParams` (obligatoire). Un document `uploadParams` XML spécifiant les paramètres de chargement) | `description`  |  `xsd:string`  | Facultatif. Description du traitement. |
| `uploadParams` (obligatoire). Un document `uploadParams` XML spécifiant les paramètres de chargement) | `destFolder`  |  `xsd:string`  | Facultatif. Chemin du dossier cible à ajouter à une propriété de nom de fichier, en particulier pour les navigateurs et autres clients qui ne prennent pas en charge les chemins complets dans un nom de fichier. |
| `uploadParams` (obligatoire). Un document `uploadParams` XML spécifiant les paramètres de chargement) | `fileName`  |  `xsd:string`  | Facultatif. Nom du fichier cible. Il remplace la propriété filename. |
| `uploadParams` (obligatoire). Un document `uploadParams` XML spécifiant les paramètres de chargement) | `endJob`  |  `xsd:boolean`  | Facultatif. Faux par défaut. |
| `uploadParams` (obligatoire). Un document `uploadParams` XML spécifiant les paramètres de chargement) | `uploadParams`  |  `types:UploadPostJob`  | Facultatif s’il s’agit d’une demande ultérieure pour un traitement actif existant. S’il existe une tâche, `uploadParams` est ignoré et les paramètres de chargement de tâche existants sont utilisés. Voir [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Dans le bloc `<uploadPostParams>` se trouve le bloc `<uploadParams>` qui désigne le traitement des fichiers inclus.

Voir [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Bien que vous puissiez supposer que le paramètre `uploadParams` peut changer pour des fichiers individuels dans le cadre de la même tâche, ce n’est pas le cas. Utilisez les mêmes paramètres de `uploadParams` pour l’ensemble de la tâche.

La requête POST initiale d’une nouvelle tâche de chargement doit spécifier le paramètre `jobName`, de préférence en utilisant un nom de tâche unique afin de simplifier l’interrogation sur le statut des tâches et les requêtes de journal de tâches ultérieures. D’autres requêtes POST pour la même tâche de chargement doivent spécifier le paramètre `jobHandle` au lieu de `jobName`, à l’aide de la valeur `jobHandle` renvoyée par la requête initiale.

La requête POST finale pour une tâche de chargement doit définir le paramètre `endJob` sur true afin qu’aucun fichier ultérieur ne soit POST pour cette tâche. Cela permet à son tour à la tâche de se terminer immédiatement après l’ingestion de tous les fichiers POSTed. Dans le cas contraire, la tâche expire si aucune requête POST supplémentaire n’est reçue dans les 30 minutes.

## Réponse UploadPOST {#section-421df5cc04d44e23a464059aad86d64e}

Pour une requête POST réussie, le corps de la réponse est un document `uploadPostReturn` XML, comme le spécifie le schéma XSD dans ce qui suit :

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

Le `jobHandle` renvoyé est transmis dans le paramètre `uploadPostParams`/ `jobHandle` pour toutes les requêtes POST suivantes pour le même traitement. Vous pouvez également l’utiliser pour interroger le statut des tâches avec l’opération `getActiveJobs` ou pour interroger les journaux de tâches avec l’opération `getJobLogDetails`.

En cas d’erreur lors du traitement de la requête POST, le corps de la réponse se compose de l’un des types d’erreurs d’API décrits à la section [Erreurs](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Exemple de requête POST {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## Exemple de réponse POST - succès {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Exemple de réponse POST - erreur {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

