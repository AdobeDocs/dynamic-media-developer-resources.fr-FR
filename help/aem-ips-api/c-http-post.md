---
description: Le téléchargement de fichiers dans Scene7 Production System implique une ou plusieurs requêtes HTTP POST qui configurent une tâche afin de coordonner tous les de journaux  associés aux fichiers téléchargés.
seo-description: Le téléchargement de fichiers dans Scene7 Production System implique une ou plusieurs requêtes HTTP POST qui configurent une tâche afin de coordonner tous les de journaux  associés aux fichiers téléchargés.
seo-title: Téléchargement de fichiers via HTTP POSTs vers la servlet UploadFile
solution: Experience Manager
title: Téléchargement de fichiers via HTTP POSTs vers la servlet UploadFile
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: dac273f51703fd63f1d427fbb7713fcc79bfa2c4

---


# Téléchargement de fichiers via HTTP POSTs vers la servlet UploadFile{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Le téléchargement de fichiers dans Scene7 Production System implique une ou plusieurs requêtes HTTP POST qui configurent une tâche afin de coordonner tous les de journaux  associés aux fichiers téléchargés.

Utilisez l’URL suivante pour accéder au servlet UploadFile :

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Toutes les requêtes POST pour une tâche de téléchargement doivent provenir de la même adresse IP.

**Accès aux URL pour les régions Scene7**

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

## Flux de travail de téléchargement {#section-873625b9512f477c992f5cdd77267094}

La tâche de téléchargement est composée d’un ou plusieurs POST HTTP qui utilisent une méthode commune `jobHandle` pour corréler le traitement dans la même tâche. Chaque requête est `multipart/form-data` codée et se compose des éléments de formulaire suivants :

>[!NOTE]
>
>Toutes les requêtes POST pour une tâche de téléchargement doivent provenir de la même adresse IP.

| Partie de formulaire HTTP POST | Description ||-|-||`auth`| Obligatoire. Un authHeader XML  spécifiant l’authentification et les informations client. Voir Authentification **des** requêtes sous [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
|`file params` |  Facultatif. Vous pouvez inclure un ou plusieurs fichiers à télécharger avec chaque requête POST. Chaque partie de fichier peut inclure un paramètre de nom de fichier dans l&#39;en-tête Content-Disposition utilisé comme nom de fichier  dans IPS si aucun `uploadPostParams/fileName` paramètre n&#39;est spécifié. |

| Partie de formulaire HTTP POST | nom de l’élément uploadPostParams | Type | Description ||-|-|-|-|||`uploadParams` (Obligatoire). Un `uploadParams` XML spécifiant les paramètres de transfert) | `companyHandle`|`xsd:string`| Obligatoire. Gérez le  vers lequel le fichier est téléchargé. |
|`uploadParams` (Obligatoire. Un `uploadParams` XML spécifiant les paramètres de transfert)|`jobName`|`xsd:string`| Soit `jobName` soit `jobHandle` est requis. Nom de la tâche de téléchargement. |
|`uploadParams` (Obligatoire. Un `uploadParams` XML spécifiant les paramètres de transfert)|`jobHandle`|`xsd:string`| Soit `jobName` soit `jobHandle` est requis. Traitement d’une tâche de téléchargement démarrée dans une requête précédente. |
|`uploadParams` (Obligatoire. Un `uploadParams` XML spécifiant les paramètres de transfert)|`locale`|`xsd:string`| Facultatif. Code de langue et de pays pour les  de. |
|`uploadParams` (Obligatoire. Un `uploadParams` XML spécifiant les paramètres de transfert)|`description`|`xsd:string`| Facultatif. Description de la tâche. |
|`uploadParams` (Obligatoire. Un `uploadParams` XML spécifiant les paramètres de transfert)|`destFolder`|`xsd:string`| Facultatif. Chemin d’accès  dossier pour ajouter un préfixe à une propriété de nom de fichier, en particulier pour les navigateurs et les autres clients qui ne prennent pas en charge les chemins complets dans un nom de fichier. |
|`uploadParams` (Obligatoire. Un `uploadParams` XML spécifiant les paramètres de transfert)|`fileName`|`xsd:string`| Facultatif. Nom du fichier . Remplace la propriété filename. |
|`uploadParams` (Obligatoire. Un `uploadParams` XML spécifiant les paramètres de transfert)|`endJob`|`xsd:boolean`| Facultatif. Faux par défaut. |
|`uploadParams` (Obligatoire. Un `uploadParams` XML spécifiant les paramètres de transfert)|`uploadParams`|`types:UploadPostJob`| Facultatif s’il s’agit d’une demande ultérieure pour une tâche active existante. S’il existe une tâche existante, `uploadParams` est ignorée et les paramètres de transfert de tâche existants sont utilisés. Voir [TéléchargementPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) .|

Dans le `<uploadPostParams>` bloc se trouve le `<uploadParams>` bloc qui désigne le traitement des fichiers inclus.

Voir [TéléchargementPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Bien que vous puissiez supposer que le `uploadParams` paramètre peut changer pour des fichiers individuels dans le cadre d’une même tâche, ce n’est pas le cas. Utilisez les mêmes `uploadParams` paramètres pour l’ensemble de la tâche.

La demande POST initiale pour une nouvelle tâche de téléchargement doit spécifier le `jobName` paramètre, en utilisant de préférence un nom de tâche unique afin de simplifier l’interrogation de l’état du travail et les  du journal de tâches ultérieures. Les requêtes POST supplémentaires pour la même tâche de téléchargement doivent spécifier le `jobHandle` paramètre au lieu de `jobName`, en utilisant la `jobHandle` valeur renvoyée par la requête initiale.

La dernière requête POST pour une tâche de téléchargement doit définir le `endJob` paramètre sur true afin qu’aucun fichier futur ne soit POSTed pour cette tâche. Cela permet à son tour de terminer la tâche immédiatement après l’assimilation de tous les fichiers POSTed. Sinon, la tâche expire si aucune demande POST supplémentaire n’est reçue dans les 30 minutes.

## Réponse UploadPOST {#section-421df5cc04d44e23a464059aad86d64e}

Pour une requête POST réussie, le corps de la réponse sera un `uploadPostReturn` XML, comme l’indique le schéma XSD dans les éléments suivants :

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

Le `jobHandle` résultat renvoyé est transmis dans le paramètre `uploadPostParams`/ `jobHandle` pour toutes les demandes POST suivantes pour la même tâche. Vous pouvez également l’utiliser pour interroger l’état de la tâche avec l’ `getActiveJobs` opération ou pour les journaux de tâches avec l’ `getJobLogDetails` opération.

En cas d’erreur lors du traitement de la requête POST, le corps de la réponse se compose de l’un des types d’erreur de l’API, comme décrit dans [Erreurs](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Exemple de requête POST {#section-810fe32abdb9426ba0fea488dffadd1e}

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

## Exemple de réponse POST - succès {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## Exemple de réponse POST - erreur {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

