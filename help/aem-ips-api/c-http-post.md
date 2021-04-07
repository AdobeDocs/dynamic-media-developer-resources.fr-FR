---
description: Le téléchargement de fichiers dans Dynamic Media Classic implique une ou plusieurs requêtes de POST HTTP qui configurent une tâche afin de coordonner toutes les activités de journal associées aux fichiers téléchargés.
solution: Experience Manager
title: Téléchargement de fichiers via HTTP POSTs vers le servlet UploadFile
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 3%

---

# Téléchargement de fichiers au moyen de POST HTTP vers le servlet UploadFile{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Le téléchargement de fichiers dans Dynamic Media Classic implique une ou plusieurs requêtes de POST HTTP qui configurent une tâche afin de coordonner toutes les activités de journal associées aux fichiers téléchargés.

Utilisez l’URL suivante pour accéder au servlet UploadFile :

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Toutes les demandes de POST pour une tâche de téléchargement doivent provenir de la même adresse IP.

**URL d’accès pour les régions Dynamic Media**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Emplacement géographique </p> </th> 
   <th colname="col2" class="entry"> <p>URL de production </p> </th> 
   <th colname="col3" class="entry"> <p>URL d’évaluation (à utiliser pour le développement et le test de pré-production) </p> </th> 
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

## Processus de la tâche de téléchargement {#section-873625b9512f477c992f5cdd77267094}

La tâche de téléchargement consiste en un ou plusieurs POST HTTP qui utilisent un `jobHandle` commun pour corréler le traitement dans la même tâche. Chaque requête est codée `multipart/form-data` et se compose des parties de formulaire suivantes :

>[!NOTE]
>
>Toutes les demandes de POST pour une tâche de téléchargement doivent provenir de la même adresse IP.

|  POST HTTP : partie  |  Description  |
|---|---|
| `auth`  |   Obligatoire. Document XML authHeader spécifiant l’authentification et les informations sur le client. Voir **Demande d’authentification** sous [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Facultatif. Vous pouvez inclure un ou plusieurs fichiers à télécharger avec chaque demande de POST. Chaque partie de fichier peut inclure un paramètre de nom de fichier dans l&#39;en-tête Content-Disposition utilisé comme nom de cible dans IPS si aucun paramètre `uploadPostParams/fileName` n&#39;est spécifié. |

|  POST HTTP : partie   |  nom de l’élément uploadPostParams   |  Type   |  Description   |
|---|---|---|---|
| `uploadParams` (Obligatoire. Un document XML `uploadParams` spécifiant les paramètres de transfert)   |   `companyHandle`  |  `xsd:string`  | Obligatoire. Traitez la société à laquelle le fichier est chargé.  |
| `uploadParams` (Obligatoire. Un document XML `uploadParams` spécifiant les paramètres de transfert) | `jobName`  |  `xsd:string`  | `jobName` ou `jobHandle` est requis. Nom de la tâche de téléchargement.  |
| `uploadParams` (Obligatoire. Un document XML `uploadParams` spécifiant les paramètres de transfert) | `jobHandle`  |  `xsd:string`  | `jobName` ou `jobHandle` est requis. Traitement d’une tâche de téléchargement démarrée dans une demande précédente.  |
| `uploadParams` (Obligatoire. Un document XML `uploadParams` spécifiant les paramètres de transfert) | `locale`  |  `xsd:string`  | Facultatif. Code de langue et de pays pour la localisation.  |
| `uploadParams` (Obligatoire. Un document XML `uploadParams` spécifiant les paramètres de transfert) | `description`  |  `xsd:string`  | Facultatif. Description de la tâche.  |
| `uploadParams` (Obligatoire. Un document XML `uploadParams` spécifiant les paramètres de transfert) | `destFolder`  |  `xsd:string`  | Facultatif. Chemin d’accès du dossier de cible à un préfixe de propriété de nom de fichier, en particulier pour les navigateurs et les autres clients qui ne prennent pas en charge les chemins complets dans un nom de fichier.  |
| `uploadParams` (Obligatoire. Un document XML `uploadParams` spécifiant les paramètres de transfert) | `fileName`  |  `xsd:string`  | Facultatif. Nom du fichier de cible. Remplace la propriété filename. |
| `uploadParams` (Obligatoire. Un document XML `uploadParams` spécifiant les paramètres de transfert) | `endJob`  |  `xsd:boolean`  | Facultatif. Faux par défaut. |
| `uploadParams` (Obligatoire. Un document XML `uploadParams` spécifiant les paramètres de transfert) | `uploadParams`  |  `types:UploadPostJob`  | Facultatif s’il s’agit d’une demande ultérieure pour une tâche principale existante. S’il existe une tâche existante, `uploadParams` est ignoré et les paramètres de transfert de tâche existants sont utilisés. Voir [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Dans le bloc `<uploadPostParams>` se trouve le bloc `<uploadParams>` qui désigne le traitement des fichiers inclus.

Voir [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Bien que vous puissiez supposer que le paramètre `uploadParams` peut changer pour des fichiers individuels dans le cadre de la même tâche, ce n&#39;est pas le cas. Utilisez les mêmes paramètres `uploadParams` pour la tâche entière.

La demande de POST initiale pour une nouvelle tâche de téléchargement doit spécifier le paramètre `jobName`, de préférence en utilisant un nom de tâche unique pour simplifier l’interrogation de l’état de la tâche et les requêtes du journal de tâches suivantes. Les demandes de POST supplémentaires pour la même tâche de téléchargement doivent spécifier le paramètre `jobHandle` au lieu de `jobName`, en utilisant la valeur `jobHandle` renvoyée par la demande initiale.

La demande finale du POST pour une tâche de téléchargement doit définir le paramètre `endJob` sur true afin qu’aucun fichier futur ne soit POSTé pour cette tâche. Cela permet à son tour de terminer la tâche immédiatement après l’assimilation de tous les fichiers POSTed. Dans le cas contraire, la tâche expire si aucune demande de POST supplémentaire n’est reçue dans les 30 minutes.

## Réponse UploadPOST {#section-421df5cc04d44e23a464059aad86d64e}

Pour une demande de POST réussie, le corps de la réponse sera un document XML `uploadPostReturn`, comme le spécifie le schéma XSD dans les éléments suivants :

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

Le `jobHandle` renvoyé est transmis dans le paramètre `uploadPostParams`/ `jobHandle` pour toute demande de POST ultérieure pour la même tâche. Vous pouvez également l’utiliser pour interroger l’état de la tâche avec l’opération `getActiveJobs` ou pour requête des journaux de tâches avec l’opération `getJobLogDetails`.

En cas d&#39;erreur lors du traitement de la demande du POST, le corps de la réponse se compose de l&#39;un des types d&#39;erreur de l&#39;API, comme décrit dans [Faults](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Exemple de requête de POST {#section-810fe32abdb9426ba0fea488dffadd1e}

```
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

## Exemple de réponse du POST - succès {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Exemple de réponse du POST - erreur {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
