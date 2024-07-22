---
title: Nouveaux ajouts et modifications
description: Décrit les modifications nouvelles et mises en oeuvre pour l’API IPS v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# Nouveaux ajouts et modifications{#new-additions-and-changes}

Décrit les modifications nouvelles et mises en oeuvre pour l’API IPS v4.0.

Mise en oeuvre de versions d’API côte à côte avec des WSDL et des espaces de noms de schéma distincts.

* Versions API précédentes : `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Version SPS 4.0 : `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Ajout du champ `PostScriptOptions/alpha` .

Ajout des propriétés `VideoRootUrl` et `SwfRootUrl` pour l’opération `getProperty`.

Ajout des paramètres facultatifs `appName` et `appVersion` à `authHeader` pour effectuer le suivi de l’application d’appel. Ajout de la journalisation à `ipsApiService.log`.

Ajout d’un paramètre facultatif `serviceUrl` au servlet de génération WSDL. Ce paramètre est utile pour le débogage des proxys. Par exemple : `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Mise en oeuvre de l’opération `getZipEntries`.

Mise en oeuvre de plages de recherche et de valeurs de comparaison saisies pour les conditions de champ système.

Ajout d’une constante de chaîne de type de ressource `'Asset'`, principalement pour autoriser les champs de métadonnées interressources.

Mise en oeuvre du paramètre `trashState` pour `searchAssets`.

Mise en oeuvre de l’opération `getAssetPublishHistory`.

Ajout de l’en-tête facultatif `faultHttpStatusCode` SOAP pour activer la gestion des erreurs dans Flex. Pour Flex, utilisez `<faultHttpStatusCode>200</faultHttpStatusCode>`. Le code d’état par défaut pour les réponses d’erreur est `500 (Internal Server Error)`.

Ajout d’opérations pour restaurer les ressources de la corbeille et les ressources vides de la corbeille.

Mise en oeuvre des opérations CRUD.

Ajout de l’indicateur enabled au type `ImageMap` et à l’opération `saveImageMap`.

Ajout de la prise en charge des tâches Optimiser les fichiers restants.

Ajout de `setAssetsPublishState` pour les mises à jour de l’état de publication en masse.

Ajout de `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Opération `saveMetadataField` obsolète en faveur des nouvelles opérations `createMetadataField` et `updateMetadataField`.

Mise en oeuvre de l’opération de suppression par lots `deleteAssetsParam`.

Mise en oeuvre de l’opération de déplacement par lots `moveAssetsParam`.

Mise en oeuvre de l’opération `deleteMetadataField`.

Mise en oeuvre des opérations `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat`.

Mise en oeuvre de `getAssetCounts`.

Ajout de la prise en charge de `setImageSetMembers` pour l’inclusion de membres `RenderSet` dans les ressources `ImageSet`.

Ajout de l’opération `replaceImage`.

Ajout de l’opération `copyImage`.

Ajout de `setUrlModifier` champs operation et `urlModifier/urlPostApplyModifier` pour `LayerViewInfo`, `TemplateInfo` et `WatermarkInfo`.

Ajout de l’opération `createDerivedAsset`. Actuellement, `ownerHandle` doit référencer une ressource Image et le type peut être `AdjustedView` ou `LayerView`.

Ajout de l’opération `createTemplate`. Appelez pour créer des ressources de modèle ou de filigrane.

Paramètres de la société IPS, `CompanySettings`, portés à l’API de services Web.

Ajout de l’indicateur de filtre `excludeByproducts` à l’opération `searchAssets`. La définition de cet indicateur sur true exécute `PSDlayer` images et images arrachées par le PDF.

Ajout de l’opération `getGenerationInfo`.

Ajout du nom de propriété `SystemMessage` à l’opération `getProperty`.

Modification de certaines constantes de chaîne de type de ressource pour qu’elles correspondent aux champs Asset Info correspondants.

* WordDoc : Word
* ExcelDoc : Excel
* PowerPointDoc : PowerPoint
* RTFoc : Rtf

Format de résultat modifié des opérations par lots pour résumer les succès, les avertissements et les erreurs.

Mise en oeuvre de l’opération de métadonnées de lot `batchSetAssetMetadata`.

Mise en oeuvre de la prise en charge des données spécifiques à l’application.

Mise en oeuvre de la prise en charge des indicateurs booléens pour `createTemplate`, `extendLayers` et `extractText` pour les tâches de transfert afin de contrôler le processus de traitement Photoshop (similaire aux modifications pour l’ajout de chargements de fichiers).

Mise en oeuvre des opérations `setImageMaps` et `setZoomTargets`.

Mise en oeuvre des opérations `ViewerPreset`. Les types reconnus sont les suivants :

* `VideoPlayer` (La vidéo publie uniquement ces visionneuses.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Les habillages des visionneuses prennent en charge deux paramètres : `skinFg` et `skinBg`. Le code principal effectue tout le traitement nécessaire pour maintenir la compatibilité ascendante.

Mise en oeuvre de l’opération `getAssociatedAssets`.

Ajout du type de tâche `ReprocessAssets` pour permettre le retraitement des fichiers sources originales précédemment téléchargés, y compris la réactualisation des PDF et la réoptimisation des images.

Type de champ `PropertySetType` renommé `propertyType`. Ce changement de nom affecte le paramètre `createPropertySetType` et la réponse `getPropertySetType/getPropertySetTypes`.

Mise en oeuvre de l’opération `batchSetImageFields` pour prendre en charge la définition des données utilisateur de l’image et d’autres champs d’image modifiables.

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

Mise en oeuvre de l’opération `getActivePublishContexts`. Cette opération renvoie un tableau de noms de contexte de publication avec des serveurs de publication actifs pour la société spécifiée. Les noms de contexte de publication actuels sont :

* `ImageServing`
* `ImageRendering`
* `Video`

Mise en oeuvre de l’opération `getSearchStrings`. Elle renvoie un tableau de chaînes de recherche pour la ressource donnée.

Ajout de paramètres régionaux pour les tâches et d’un mécanisme pour définir les paramètres régionaux des opérations de l’API. La chaîne locale doit être formatée sous la forme `<language_code>[-<country_code>]`. Le code de langue est un code à deux lettres minuscules, comme spécifié par la norme ISO-639, et le code de pays facultatif est un code à deux lettres majuscules, comme spécifié par la norme ISO-3166.

Ajout du paramètre régional facultatif à l’en-tête de SOAP `authHeader` pour définir les paramètres régionaux des opérations API. Si ce paramètre n’est pas présent, l’en-tête HTTP `Accept-Language` est utilisé. Si cet en-tête n’est pas non plus présent, le paramètre régional par défaut du serveur IPS est utilisé.

Ajout de la prise en charge de la fonction get/set pour les champs de métadonnées fortement tapés.

Mise en oeuvre de la prise en charge des en-têtes SOAP et HTTP pour le contrôle de réponse gzip.

Ajout de l’indicateur `gzipResponse` à `authHeader`. S’il n’est pas présent, l’API vérifie l’en-tête HTTP `Accept-Encoding`.

Ajout de la prise en charge des conditions de champ de métadonnées de recherche de ressources fortement typées.

* Pour tous les types de champ, la valeur peut être transmise avec un opérateur de comparaison de chaînes ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Pour les champs booléens, `boolVal` peut être transmis avec l’opération `Equals`.
* Pour les champs Int, `longVal` peut être transmis avec un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minLong/maxLong` peut l’être avec des opérations de plage numérique ( `Between, NotBetween`).
* Pour les champs flottants, `doubleVal` peut être transmis avec un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minDouble/maxDouble` peut l’être avec des opérations de plage numérique ( `Between, NotBetween`).
* Pour les champs Date, vous pouvez transmettre `dateVal` avec un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou vous pouvez transmettre minDate/maxDate avec une plage numérique ( `Between, NotBetween`).

Ajout des champs description, `jobSubType` et `originalJobName` au type `JobLog`.

* `originalJobName` est le nom de la tâche envoyée à `submitJob` (sans suffixes d’unicité ni noms de tâche consécutifs).
* `jobSubType` est utilisé uniquement par les `ImageServingPublishJob` tâches (où il s’agit de l’une des `full`, `increment, fullwithsearch,` ou `fulloverride`).
* `description` est une chaîne vide pour tous les types de tâche, mais elle contient éventuellement des informations de tâche récapitulatives, telles que le chemin de chargement.

En outre, les champs suivants ne sont pas inclus avec `getJobLogs` et `getJobLogDetails`. Dans les versions précédentes, elles n’étaient disponibles qu’avec `getJobLogDetails`.

* `endDate` (si la tâche est terminée).
* `fileDuplicateCount` (auparavant, il s’agissait toujours de `0` avec `getJobLogs`)
* `fileUpdateCount` (auparavant toujours `0` avec `getJobLogs` et inclus dans `fileSuccessCount` ; il est désormais divisé en champs distincts).

Ajout du champ assetHandle au type `JobLogDetail`.

Ajout du paramètre de description facultatif à `submitJob`. Ce paramètre est transmis pour récupération dans `getScheduledJobs`, `getActiveJobs` et `getJobLogs`.

Le champ du système de SKU a été obsolète. Le champ est ignoré s’il est transmis en tant que `SystemFieldCondition` à `searchAssets`.

Ajout du filtre `excludeAssetTypeArray` à `searchAssets`.

Ajout du type `MaskInfo` à `Asset`.

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
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Document Microsoft® Word pour les fichiers se terminant par .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Document Excel Microsoft® pour les fichiers se terminant par .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Document Microsoft® PowerPoint pour les fichiers se terminant par .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFoc </span> </p> </td> 
   <td colname="col2"> <p>Fichier RTF pour les fichiers chargés se terminant par .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ajout d’options supplémentaires à `UploadDirectoryJob` et `UploadUrlsJob` pour contrôler le traitement indépendant des fichiers Postscript, Illustrator et PDF. Toutes les tâches existantes fournissent les paramètres nécessaires à chacun des trois pipelines de traitement afin qu’ils fonctionnent exactement comme aujourd’hui. Le bloc `PostScriptOptions` d&#39;origine est utilisé pour définir le traitement des fichiers Illustrator et EPS/PS. Vous pouvez éventuellement fournir des blocs d’options de fichier spécifiques pour spécifier le traitement. La liste des modifications comprend :

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
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Aucun </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Pixelliser </span> (par défaut) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Ne gérez que la ressource et ne créez aucun produit dérivé lors du téléchargement. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Effectuez le rendu du fichier EPS et PostScript dans une image à la résolution et à l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Facultatif. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Cet événement est pris en compte lors de la pixellisation du fichier dans une image. Il crée un arrière-plan transparent si le fichier d’origine est défini de cette manière pour superposer des logos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Aucun </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Pixelliser </span> (par défaut) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Ne gérez que la ressource et ne créez aucun produit dérivé lors du téléchargement. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Effectuez le rendu du fichier dans une image à la résolution et à l’espace colorimétrique prévus. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterisation de la résolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espace colorimétrique cible pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Facultatif. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Cet événement est pris en compte lors de la pixellisation du fichier dans une image. Crée un arrière-plan transparent si le fichier d’origine est défini de cette manière pour créer des logos superposés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Aucun </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Pixelliser </span> (par défaut) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Ne gérez que la ressource et ne créez aucun produit dérivé lors du téléchargement. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Effectuez le rendu du fichier dans une image à la résolution et à l’espace colorimétrique prévus. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterisation de la résolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espace colorimétrique cible pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit s’il faut combiner plusieurs PDF de page dans un catalogue électronique après le rendu (la valeur par défaut est true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit si les mots du PDF sont extraits dans la base de données pour être ensuite fournis à un serveur de recherche (la valeur par défaut est false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez également effectuer des requêtes à partir de `getScheduledJobs`.

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
   <td colname="col2"> <p>Ne répondez pas par gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>Réponse Gzip uniquement si authHeader/gzipResponse est vrai. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip si authHeader/gzipResponse est défini sur true ou si aucun en-tête gzipResponse n’est présent et que l’en-tête HTTP Accept-Encoding inclut gzip. (Par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>Toujours gzip, quelle que soit la valeur de l’en-tête. Utilisez cette valeur uniquement à des fins de débogage. </p> </td> 
  </tr> 
 </tbody> 
</table>
