---
description: Décrit les modifications nouvelles et mises en oeuvre pour l'API IPS v4.0.
seo-description: Décrit les modifications nouvelles et mises en oeuvre pour l'API IPS v4.0.
seo-title: Nouveaux ajouts et modifications
solution: Experience Manager
title: Nouveaux ajouts et modifications
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 2%

---


# Nouveaux ajouts et modifications{#new-additions-and-changes}

Décrit les modifications nouvelles et mises en oeuvre pour l&#39;API IPS v4.0.

Mise en oeuvre de versions d’API côte à côte avec des WSDL et des espaces de nommage de schéma distincts.

* Versions d’API précédentes : `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Version de SPS 4.0 : `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Champ Ajouté `PostScriptOptions/alpha` .

Ajouté `VideoRootUrl` et `SwfRootUrl` propriétés pour `getProperty` l’opération.

Ajouté les paramètres facultatifs `appName` et `appVersion` pour `authHeader` effectuer le suivi de l&#39;application d&#39;appel. Connexion Ajoutée à `ipsApiService.log`.

Ajouté un `serviceUrl` paramètre facultatif à la servlet de génération WSDL. Ceci est particulièrement utile pour les proxies de débogage. Par exemple: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Opération mise en oeuvre `getZipEntries` .

Mise en oeuvre de plages de recherche et de valeurs de comparaison saisies pour les conditions de champ système.

Constante de chaîne de type de `'Asset'` ressource Ajoutée, principalement pour autoriser les champs de métadonnées entre fichiers.

Mise en oeuvre du `trashState` paramètre pour `searchAssets`.

Opération mise en oeuvre `getAssetPublishHistory` .

Ajouté de l’en-tête `faultHttpStatusCode` SOAP facultatif pour activer la gestion des pannes dans Flex. Pour Flex, utilisez `<faultHttpStatusCode>200</faultHttpStatusCode>`. Le code d&#39;état par défaut pour les réponses aux erreurs est `500 (Internal Server Error)`.

Opérations Ajoutées pour restaurer les fichiers de la corbeille et les fichiers vides de la corbeille.

Mise en oeuvre des opérations CRUD.

Indicateur activé Ajouté pour le `ImageMap` type et l&#39; `saveImageMap` opération.

Prise en charge Ajoutée des tâches Optimiser les fichiers restants.

Ajouté `setAssetsPublishState` pour les mises à jour d’état de publication en bloc.

Added `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Opération obsolète en faveur de nouvelles `saveMetadataField``createMetadataField` `updateMetadataField` opérations.

Mise en oeuvre de l&#39;opération de suppression `deleteAssetsParam` par lot.

Mise en oeuvre de l&#39;opération de déplacement `moveAssetsParam` par lot.

Opération mise en oeuvre `deleteMetadataField` .

Mise en oeuvre `get/setImageRenderingPublishSettings`d&#39; `get/set/create/updateVignettePublishFormat` opérations.

Implemented `getAssetCounts`.

Prise en charge Ajoutée de `setImageSetMembers` l’inclusion de `RenderSet` membres dans `ImageSet` les ressources.

Opération Ajoutée. `replaceImage`

Opération Ajoutée. `copyImage`

`setUrlModifier` opération et `urlModifier/urlPostApplyModifier` champs Ajoutés pour `LayerViewInfo`, `TemplateInfo`et `WatermarkInfo`.

Opération Ajoutée. `createDerivedAsset` Actuellement, il `ownerHandle` doit référencer un fichier d’image et le type peut être `AdjustedView` ou `LayerView`.

Opération Ajoutée. `createTemplate` Actuellement, il est possible de l’appeler pour créer des ressources de modèle ou de filigrane.

Paramètres de la société IPS, `CompanySettings`portés à l&#39;API des services Web.

Indicateur `excludeByproducts` de filtre Ajouté pour `searchAssets` l&#39;opération. La définition de cet indicateur sur true exécute `PSDlayer` les images et les images pixellisées au format PDF.

Opération Ajoutée. `getGenerationInfo`

Nom de `SystemMessage` propriété Ajouté à `getProperty` l&#39;opération.

Modification de certaines constantes de chaîne de type de ressource pour qu’elles correspondent aux champs Informations sur le fichier correspondants.

* WordDoc : Word
* ExcelDoc : Excel
* PowerPointDoc : PowerPoint
* RTFDoc : Rtf

Format de résultat modifié des opérations par lot pour résumer les réussites, les avertissements et les erreurs.

Mise en oeuvre de l’opération de métadonnées `batchSetAssetMetadata` par lot.

Mise en oeuvre de la prise en charge des données spécifiques à l’application.

Mise en oeuvre de la prise en charge des indicateurs booléens pour `createTemplate`, `extendLayers`et `extractText` pour les tâches de transfert afin de contrôler le processus de traitement Photoshop (comme les modifications pour les ajouts de fichiers téléchargés).

Mise en oeuvre `setImageMaps` et `setZoomTargets` opérations.

Opérations mises en oeuvre `ViewerPreset` . Les types reconnus sont les suivants :

* `VideoPlayer` (La vidéo publie uniquement ces visionneuses.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Les habillages des visionneuses prennent en charge deux paramètres : `skinFg` et `skinBg`. Le code principal effectue tout le traitement nécessaire pour maintenir la compatibilité ascendante.

Opération mise en oeuvre `getAssociatedAssets` .

Type de `ReprocessAssets` tâche Ajouté pour permettre le retraitement des fichiers source principaux précédemment téléchargés, y compris la récupération de fichiers PDF et la réoptimisation des images.

Le type de `PropertySetType` champ a été renommé `propertyType`. Cela affecte le `createPropertySetType` paramètre et la `getPropertySetType/getPropertySetTypes` réponse.

Mise en oeuvre `batchSetImageFields` d’une opération de prise en charge de la définition des données utilisateur de l’image et d’autres champs d’image modifiables.

47 Ajoute le champ fileSize à divers types d’informations sur les ressources :

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

Opération mise en oeuvre `getActivePublishContexts` . Cette opération renvoie un tableau de noms de contexte de publication avec des serveurs de publication actifs pour la société spécifiée. Les noms de contexte de publication actuels sont :

* `ImageServing`
* `ImageRendering`
* `Video`

Opération mise en oeuvre `getSearchStrings` . Elle renvoie un tableau de chaînes de recherche pour la ressource donnée.

Paramètres régionaux Ajoutés pour les tâches et mécanisme permettant de définir les paramètres régionaux pour les opérations d’API. La chaîne de paramètres régionaux doit être formatée `<language_code>[-<country_code>]`. Le code de langue est un code à deux lettres minuscule, comme indiqué par ISO-639, et le code de pays facultatif est un code à deux lettres majuscule, comme spécifié par ISO-3166.

Ajouté le paramètre régional facultatif dans l’en-tête `authHeader` SOAP pour définir les paramètres régionaux des opérations d’API. Si ce paramètre n’est pas présent, l’en-tête HTTP `Accept-Language` sera utilisé. Si cet en-tête n&#39;est pas non plus présent, les paramètres régionaux par défaut du serveur IPS sont utilisés.

Prise en charge Ajoutée de l’obtention et de la définition des champs de métadonnées fortement typés.

Mise en oeuvre de la prise en charge des en-têtes SOAP et HTTP pour le contrôle des réponses gzip.

Indicateur Ajouté à `gzipResponse` `authHeader`. S&#39;il n&#39;est pas présent, l&#39;API vérifie également l&#39;en-tête HTTP `Accept-Encoding` .

Prise en charge Ajoutée de searchAssets pour les conditions de champ de métadonnées fortement typées.

* Pour tous les types de champs, la valeur peut être transmise avec un opérateur de comparaison de chaînes ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Pour les champs booléens, `boolVal` peut être transmis avec l’ `Equals` op.
* Pour les champs Int, `longVal` il est possible de transmettre l’information à l’aide d’un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minLong/maxLong` de transmettre l’information à l’aide d’une plage numérique ( `Between, NotBetween`).
* Pour les champs flottants, `doubleVal` il est possible de transmettre un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minDouble/maxDouble` de transmettre un opérateur de plage numérique ( `Between, NotBetween`).
* Pour les champs Date, vous pouvez transmettre `dateVal` un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou transmettre minDate/maxDate avec une plage numérique ( `Between, NotBetween`).

Description, `jobSubType`et `originalJobName` champs Ajoutés à `JobLog` saisir.

* `originalJobName` est le nom de la tâche envoyée à `submitJob` (sans suffixes d’unicité ni noms de tâche consécutifs).
* `jobSubType` n’est actuellement utilisée que par `ImageServingPublishJob` les tâches (où il s’agit d’une des `full`, `increment, fullwithsearch,` ou `fulloverride`).
* `description` est actuellement une chaîne vide pour tous les types de tâche, mais contiendra éventuellement des informations de tâche récapitulatives, telles que le chemin d’accès au téléchargement.

En outre, les champs suivants ne sont pas inclus avec les deux `getJobLogs` et `getJobLogDetails`. Dans les versions précédentes, ils n&#39;étaient disponibles qu&#39;avec `getJobLogDetails`.

* `endDate` (si la tâche est terminée).
* `fileDuplicateCount` (auparavant, c&#39;était toujours `0` avec `getJobLogs`)
* `fileUpdateCount` (auparavant était toujours `0` avec `getJobLogs` et inclus dans `fileSuccessCount`; elle est maintenant divisée en champs distincts).

Champ assetHandle Ajouté à `JobLogDetail` saisir.

Paramètre de description facultatif Ajouté à `submitJob`. Elle est transmise pour récupération dans `getScheduledJobs`, `getActiveJobs`et `getJobLogs`.

Déconseillé au champ du système SKU. Le champ est ignoré s’il est transmis en tant que valeur `SystemFieldCondition` à `searchAssets`.

Ajouté `excludeAssetTypeArray` le filtre sur `searchAssets`.

Type Ajouté sur `MaskInfo` `Asset`.

Nouveaux types de ressources Ajoutés pour la gestion par IPS :

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
   <td colname="col2"> <p>Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Postscript </span> </p> </td> 
   <td colname="col2"> <p>Fichiers EPS et PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>document Microsoft Word pour les fichiers se terminant par .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>document Microsoft Excel pour les fichiers se terminant par .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>document Microsoft PowerPoint pour les fichiers se terminant par .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>fichier RTF pour les fichiers téléchargés se terminant par .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ajouté d’autres options pour `UploadDirectoryJob` et `UploadUrlsJob` pour contrôler le traitement des fichiers Postscript, Illustrator et PDF indépendamment. Tous les emplois existants fourniront les paramètres nécessaires à chacun des trois pipelines de transformation afin qu&#39;ils fonctionnent exactement comme aujourd&#39;hui. Le `PostScriptOptions` bloc d’origine permet de définir le traitement des fichiers Illustrator et EPS/PS. Vous pouvez éventuellement fournir des blocs d&#39;options de fichier spécifiques pour spécifier le traitement. La liste des modifications comprend :

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processus </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Aucun </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Pixelliser </span>(par défaut) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Ne gérez que la ressource et ne créez pas de dérivés au moment du téléchargement. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Générer le fichier EPS et PostScript dans une image à la résolution et à l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Facultatif. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Cet effet est appliqué lors de la pixellisation du fichier dans une image. Il créera un arrière-plan transparent si le fichier d'origine est défini de cette façon pour l'incrustation de logos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processus </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Aucun </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Pixelliser </span> (par défaut) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Ne gérez que la ressource et ne créez pas de dérivés au moment du téléchargement. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Générer le fichier dans une image à la résolution et à l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> résolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entier&gt; </span> </p> </td> 
   <td colname="col4"> <p>Pixellisation de la résolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Espace colorimétrique </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espace colorimétrique de la Cible pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Facultatif. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Cet effet est affecté lors de la pixellisation du fichier dans une image. Crée un arrière-plan transparent si le fichier d’origine est défini de cette façon pour créer des logos superposés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> Options PDFO </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processus </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Aucun </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Pixelliser </span> (par défaut) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Ne gérez que la ressource et ne créez pas de dérivés au moment du téléchargement. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Générer le fichier dans une image à la résolution et à l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> résolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entier&gt; </span> </p> </td> 
   <td colname="col4"> <p>Pixellisation de la résolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Espace colorimétrique </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espace colorimétrique de la Cible pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit s’il faut combiner un PDF de plusieurs pages dans un catalogue électronique après le rendu (la valeur par défaut est true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit si les mots du PDF sont extraits dans la base de données pour être ensuite fournis à un serveur de recherche (la valeur par défaut est false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez également requête depuis `getScheduledJobs`.

Modification de la propriété `webservice.gzip.response` de configuration pour qu’elle prenne l’une des valeurs suivantes :

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valeur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jamais </span> </p> </td> 
   <td colname="col2"> <p>Ne répondez pas par gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>Réponse Gzip uniquement si authHeader/gzipResponse est vrai. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> accepter </span> </p> </td> 
   <td colname="col2"> <p>Gzip si authHeader/gzipResponse est vrai ou si aucun en-tête gzipResponse n’est présent et que l’en-tête HTTP Accept-Encoding inclut gzip. (Par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toujours </span> </p> </td> 
   <td colname="col2"> <p>Toujours gzip, quelle que soit la valeur de l’en-tête. Utilisez cette valeur uniquement à des fins de débogage. </p> </td> 
  </tr> 
 </tbody> 
</table>

