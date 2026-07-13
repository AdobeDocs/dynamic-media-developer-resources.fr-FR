---
title: Nouveaux ajouts et modifications
description: Décrit les modifications nouvelles et implémentées pour l’API IPS v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
TQID: 'https://experienceleague.adobe.com/QuVnFsc1R-WcjFpnyENi6n9US7Y7V-cETwitnVsmMss'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 1207
ht-degree: 0%

---

# Nouveaux ajouts et modifications{#new-additions-and-changes}

Décrit les modifications nouvelles et implémentées pour l’API IPS v4.0.

Versions d’API côte à côte implémentées avec des WSDL et des espaces de noms de schéma distincts.

* Versions d’API précédentes : `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Version SPS 4.0 : `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Ajout d’un champ `PostScriptOptions/alpha` .

Ajout des propriétés `VideoRootUrl` et `SwfRootUrl` pour l’opération `getProperty`.

Ajout de paramètres `appName` et `appVersion` facultatifs à `authHeader` pour effectuer le suivi de l’application appelante. Ajout de la journalisation à la `ipsApiService.log`.

Ajout d’un paramètre `serviceUrl` facultatif au servlet de génération WSDL. Ce paramètre est utile pour les proxys de débogage. Par exemple : `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Mise en œuvre de l’opération `getZipEntries`.

Mise en œuvre de plages de recherche et de valeurs de comparaison saisies pour des conditions de champ système.

Ajout d’une constante de chaîne de type ressource `'Asset'`, principalement pour autoriser les champs de métadonnées inter-ressources.

Paramètre `trashState` implémenté pour `searchAssets`.

Mise en œuvre de l’opération `getAssetPublishHistory`.

Ajout d’un en-tête SOAP `faultHttpStatusCode` facultatif pour activer la gestion des pannes dans Flex. Pour Flex, utilisez `<faultHttpStatusCode>200</faultHttpStatusCode>`. Le code d&#39;état par défaut pour les réponses d&#39;erreur est `500 (Internal Server Error)`.

Ajout d’opérations visant à restaurer les ressources à partir de la corbeille et à vider les ressources de la corbeille.

Mise en œuvre des opérations CRUD.

Ajout d’un indicateur activé pour le type de `ImageMap` et l’opération de `saveImageMap`.

Ajout de la prise en charge des tâches d’optimisation des fichiers restants.

Ajout de `setAssetsPublishState` pour les mises à jour de l’état de publication en bloc.

Ajout de `ImageServingPublishSettings`, `getImageServingPublishSettings` et `setImageServingPublishSettings`.

Opération `saveMetadataField` obsolète au profit de nouvelles opérations `createMetadataField` et `updateMetadataField`.

Implémentation de `deleteAssetsParam` opération de suppression par lots.

Mise en œuvre `moveAssetsParam` opération de déplacement par lots.

Mise en œuvre de l’opération `deleteMetadataField`.

Mise en œuvre `get/setImageRenderingPublishSettings` opérations `get/set/create/updateVignettePublishFormat`.

Mise en œuvre de `getAssetCounts`.

Ajout de la prise en charge des `setImageSetMembers` pour l’inclusion de membres `RenderSet` dans les ressources `ImageSet`.

Ajout d’une opération `replaceImage`.

Ajout d’une opération `copyImage`.

Ajout de champs d’opération de `setUrlModifier` et de `urlModifier/urlPostApplyModifier` pour `LayerViewInfo`, `TemplateInfo` et `WatermarkInfo`.

Ajout d’une opération `createDerivedAsset`. Actuellement, le `ownerHandle` doit référencer une ressource d’image et le type peut être `AdjustedView` ou `LayerView`.

Ajout d’une opération `createTemplate`. Appel pour créer des ressources de modèle ou de filigrane.

Paramètres de la société IPS, `CompanySettings`, transférés vers l’API de services Web.

Ajout de l’indicateur de filtre `excludeByproducts` à l’opération `searchAssets`. La définition de cet indicateur sur true exécute `PSDlayer` images et les images pixellisées PDF.

Ajout d’une opération `getGenerationInfo`.

Ajout du nom de la propriété `SystemMessage` à l’opération `getProperty`.

Modification de certaines constantes de chaîne de type de ressource pour qu’elles correspondent aux champs Informations sur les ressources .

* WordDoc : Word
* ExcelDoc : Excel
* PowerPointDoc : PowerPoint
* RTFDoc : Rtf

Modification du format des résultats des opérations par lots pour résumer les succès, les avertissements et les erreurs.

Implémentation `batchSetAssetMetadata` l’opération de métadonnées par lots.

Prise en charge implémentée pour les données spécifiques à l’application.

Mise en œuvre de la prise en charge des indicateurs booléens pour `createTemplate`, `extendLayers` et `extractText` pour les tâches de chargement afin de contrôler le processus de traitement Photoshop (similaire aux modifications pour les chargements de fichiers d’ajout).

Mise en œuvre des opérations `setImageMaps` et `setZoomTargets`.

Mise en œuvre des opérations `ViewerPreset`. Les types reconnus sont les suivants :

* `VideoPlayer` (la vidéo ne publie que ces visionneuses.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Les enveloppes de visionneuse prennent en charge deux paramètres : `skinFg` et `skinBg`. Le code du serveur principal effectue tout le traitement nécessaire pour maintenir la rétrocompatibilité.

Mise en œuvre de l’opération `getAssociatedAssets`.

Ajout d’un type de tâche `ReprocessAssets` pour permettre le retraitement des fichiers sources principaux précédemment chargés, y compris la récupération des PDF et la réoptimisation des images.

Le type de champ `PropertySetType` a été renommé `propertyType`. Ce changement de nom affecte le paramètre `createPropertySetType` et la réponse `getPropertySetType/getPropertySetTypes`.

Implémentation d’une opération `batchSetImageFields` pour prendre en charge la définition des données utilisateur d’image et d’autres champs d’image modifiables.

47 Ajout du champ fileSize à divers types d’informations sur les ressources :

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

Mise en œuvre de l’opération `getActivePublishContexts`. Cette opération renvoie un tableau de noms de contexte de publication avec des serveurs de publication actifs pour la société spécifiée. Les noms actuels du contexte de publication sont les suivants :

* `ImageServing`
* `ImageRendering`
* `Video`

Mise en œuvre de l’opération `getSearchStrings`. Elle renvoie un tableau de chaînes de recherche pour la ressource donnée.

Ajout de paramètres régionaux pour les tâches et d’un mécanisme de définition des paramètres régionaux pour les opérations de l’API. La chaîne du paramètre régional doit être formatée en tant que `<language_code>[-<country_code>]`. Le code de langue est un code à deux lettres en minuscules spécifié par la norme ISO-639, et le code de pays facultatif est un code à deux lettres en majuscules spécifié par la norme ISO-3166.

Ajout d’un paramètre régional facultatif à l’en-tête `authHeader` SOAP pour définir le paramètre régional des opérations de l’API. Si ce paramètre n’est pas présent, le `Accept-Language` d’en-tête HTTP est utilisé. Si cet en-tête n’est pas non plus présent, le paramètre régional par défaut du serveur IPS est utilisé.

Ajout de la prise en charge get/set des champs de métadonnées fortement typés.

Implémentation de la prise en charge des en-têtes SOAP et HTTP pour le contrôle de la réponse gzip.

Ajout de l’indicateur de `gzipResponse` à `authHeader`. S’il n’est pas présent, l’API vérifie l’en-tête HTTP `Accept-Encoding`.

Ajout de la prise en charge de la recherche de conditions de champ de métadonnées fortement typées dans les ressources.

* Pour tous les types de champ, la valeur peut être transmise avec un opérateur de comparaison de chaînes ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Pour les champs booléens, les `boolVal` peuvent être transmises avec l’opération `Equals`.
* Pour les champs Int, les `longVal` peuvent être transmises avec un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou les `minLong/maxLong` peuvent être transmises avec des opérations de plage numérique ( `Between, NotBetween`).
* Pour les champs flottants, les `doubleVal` peuvent être transmises avec un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou les `minDouble/maxDouble` peuvent être transmises avec des opérations de plage numérique ( `Between, NotBetween`).
* Pour les champs de date, vous pouvez transmettre des `dateVal` avec un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou transmettre des opérations minDate/maxDate avec une plage numérique ( `Between, NotBetween`).

Ajout de champs de description, de `jobSubType` et de `originalJobName` au type de `JobLog`.

* `originalJobName` est le nom du traitement envoyé à `submitJob` (sans suffixes d’unicité ni noms de traitements de suivi).
* `jobSubType` n’est utilisé que par les tâches de `ImageServingPublishJob` (lorsqu’il s’agit d’une tâche `full`, `increment, fullwithsearch,` ou `fulloverride`).
* `description` est une chaîne vide pour tous les types de tâche, mais elle contient finalement des informations récapitulatives sur la tâche, telles que le chemin de chargement.

En outre, les champs suivants ne sont pas inclus à la fois dans `getJobLogs` et `getJobLogDetails`. Dans les versions précédentes, ils n’étaient disponibles qu’avec `getJobLogDetails`.

* `endDate` (si le traitement est terminé).
* `fileDuplicateCount` (auparavant, il était toujours `0` avec `getJobLogs`)
* `fileUpdateCount` (auparavant, il était toujours `0` avec `getJobLogs` et inclus dans `fileSuccessCount` ; il est désormais divisé en champs distincts).

Ajout du champ assetHandle au type de `JobLogDetail`.

Ajout d’un paramètre de description facultatif à `submitJob`. Ce paramètre est transmis pour récupération dans `getScheduledJobs`, `getActiveJobs` et `getJobLogs`.

Champ système de SKU obsolète. Le champ est ignoré s’il est transmis en tant que `SystemFieldCondition` à `searchAssets`.

Ajout d’un filtre `excludeAssetTypeArray` à `searchAssets`.

Ajout du type de `MaskInfo` à `Asset`.

Ajout de nouveaux types de ressources pour la gestion par IPS :

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Type de fichier </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Fichier Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>Fichiers EPS et PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> WordDoc </p> </td> 
   <td colname="col2"> <p>Document ® Word pour les fichiers se terminant par .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Document ® Excel pour les fichiers se terminant par .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Document ® PowerPoint pour les fichiers se terminant par .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> RTFDoc <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Fichier RTF pour les fichiers chargés se terminant par .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ajout d’options supplémentaires aux `UploadDirectoryJob` et `UploadUrlsJob` pour contrôler indépendamment le traitement des fichiers Postscript, Illustrator et PDF. Toutes les tâches existantes fournissent les paramètres nécessaires à chacun des trois pipelines de traitement afin qu’ils fonctionnent exactement comme aujourd’hui. Le bloc `PostScriptOptions` d’origine est utilisé pour définir le traitement des fichiers Illustrator et EPS/PS. Vous pouvez éventuellement fournir des blocs d’options de fichier spécifiques pour spécifier le traitement. La liste des modifications comprend :

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Champ </p> </th> 
   <th colname="col2" class="entry"> <p>Paramètre </p> </th> 
   <th colname="col3" class="entry"> <p>Valeur </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Aucune </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Pixelliser </span> (par défaut) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gérez uniquement la ressource et ne créez aucun dérivé lors du chargement. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Effectuez le rendu du fichier EPS et PostScript dans une image à la résolution et dans l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Facultatif. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Prend effet lors de la pixellisation du fichier dans une image. Cela crée un arrière-plan transparent si le fichier d’origine est défini de cette manière pour superposer les logos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> </span> de processus <span class="codeph"> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Aucune </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Pixelliser le </span> (par défaut) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gérez uniquement la ressource et ne créez aucun dérivé lors du chargement. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Effectuez le rendu du fichier dans une image à la résolution et dans l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entier&gt; </span> </p> </td> 
   <td colname="col4"> <p>Pixellisation de la résolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espace colorimétrique cible pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Facultatif. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Prend effet lors de la pixellisation du fichier dans une image. Crée un arrière-plan transparent si le fichier d’origine est ainsi défini pour créer des logos de recouvrement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> </span> de processus <span class="codeph"> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Aucune </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Pixelliser le </span> (par défaut) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gérez uniquement la ressource et ne créez aucun dérivé lors du chargement. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Effectuez le rendu du fichier dans une image à la résolution et dans l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entier&gt; </span> </p> </td> 
   <td colname="col4"> <p>Pixellisation de la résolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espace colorimétrique cible pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit s’il faut combiner un PDF à plusieurs pages dans un catalogue électronique après le rendu (la valeur par défaut est true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit si les mots du PDF sont extraits dans la base de données pour être ultérieurement fournis à un serveur de recherche (la valeur par défaut est false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez également effectuer une requête à partir de `getScheduledJobs`.

Modification de la propriété de configuration `webservice.gzip.response` pour prendre l’une des valeurs suivantes :

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valeur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>Ne pas exécuter la réponse Gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>Réponse Gzip uniquement si authHeader/gzipResponse est true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip si authHeader/gzipResponse a la valeur true ou si aucun en-tête gzipResponse n’est présent et que l’en-tête HTTP Accept-Encoding inclut gzip. (Par Défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>Toujours la réponse Gzip, quelles que soient les valeurs d’en-tête. Utilisez cette valeur uniquement à des fins de débogage. </p> </td> 
  </tr> 
 </tbody> 
</table>

