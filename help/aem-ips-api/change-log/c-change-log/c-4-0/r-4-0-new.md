---
description: Décrit les modifications nouvelles et mises en oeuvre pour l'API IPS v4.0.
solution: Experience Manager
title: Nouveaux ajouts et modifications
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 2%

---

# Nouveaux ajouts et modifications{#new-additions-and-changes}

Décrit les modifications nouvelles et mises en oeuvre pour l&#39;API IPS v4.0.

Mise en oeuvre de versions d’API côte à côte avec des WSDL et des espaces de nommage de schéma distincts.

* Versions d’API précédentes : `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Version de SPS 4.0 : `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Champ `PostScriptOptions/alpha` Ajouté.

Propriétés `VideoRootUrl` et `SwfRootUrl` Ajoutées pour l&#39;opération `getProperty`.

Ajouté les paramètres facultatifs `appName` et `appVersion` à `authHeader` pour effectuer le suivi de l&#39;application d&#39;appel. Connexion Ajoutée à `ipsApiService.log`.

Ajouté un paramètre facultatif `serviceUrl` à la servlet de génération WSDL. Ceci est particulièrement utile pour les proxies de débogage. Par exemple: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Mise en oeuvre de l&#39;opération `getZipEntries`.

Mise en oeuvre de plages de recherche et de valeurs de comparaison saisies pour les conditions de champ système.

Constante de chaîne de type de ressource `'Asset'` Ajoutée, principalement pour autoriser les champs de métadonnées entre fichiers.

Mise en oeuvre du paramètre `trashState` pour `searchAssets`.

Mise en oeuvre de l&#39;opération `getAssetPublishHistory`.

En-tête SOAP facultatif `faultHttpStatusCode` Ajouté pour activer la gestion des erreurs dans Flex. Pour Flex, utilisez `<faultHttpStatusCode>200</faultHttpStatusCode>`. Le code d&#39;état par défaut pour les réponses aux erreurs est `500 (Internal Server Error)`.

Opérations Ajoutées de restauration des actifs de la corbeille et des actifs vides de la corbeille.

Mise en oeuvre des opérations CRUD.

Indicateur activé Ajouté pour le type `ImageMap` et l&#39;opération `saveImageMap`.

Prise en charge Ajoutée des tâches Optimiser les fichiers restants.

`setAssetsPublishState` Ajouté pour les mises à jour d’état de publication en bloc.

Ajouté `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Opération `saveMetadataField` obsolète en faveur de nouvelles opérations `createMetadataField` et `updateMetadataField`.

Mise en oeuvre de l&#39;`deleteAssetsParam` opération de suppression par lot.

Mise en oeuvre de l&#39;opération de déplacement par lot `moveAssetsParam`.

Mise en oeuvre de l&#39;opération `deleteMetadataField`.

Mise en oeuvre des opérations `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat`.

Mise en oeuvre de `getAssetCounts`.

Prise en charge Ajoutée de `setImageSetMembers` pour l&#39;inclusion de membres `RenderSet` dans les ressources `ImageSet`.

Opération `replaceImage` Ajoutée.

Opération `copyImage` Ajoutée.

Champs `setUrlModifier` et `urlModifier/urlPostApplyModifier` Ajoutés pour `LayerViewInfo`, `TemplateInfo` et `WatermarkInfo`.

Opération `createDerivedAsset` Ajoutée. Actuellement, `ownerHandle` doit faire référence à un fichier d’image et le type peut être `AdjustedView` ou `LayerView`.

Opération `createTemplate` Ajoutée. Actuellement, il est possible de l’appeler pour créer des ressources de modèle ou de filigrane.

Paramètres de la société IPS, `CompanySettings`, portés à l&#39;API des services Web.

Indicateur de filtre `excludeByproducts` Ajouté à l&#39;opération `searchAssets`. La définition de cet indicateur sur true exécute `PSDlayer` les images et les images pixellisées au format PDF.

Opération `getGenerationInfo` Ajoutée.

Nom de propriété `SystemMessage` Ajouté à l&#39;opération `getProperty`.

Modification de certaines constantes de chaîne de type de ressource pour qu’elles correspondent aux champs Informations sur le fichier correspondants.

* WordDoc : Word
* ExcelDoc : Excel
* PowerPointDoc : PowerPoint
* RTFDoc : Rtf

Format de résultat modifié des opérations par lot pour résumer les réussites, les avertissements et les erreurs.

Mise en oeuvre de l&#39;opération de métadonnées de lot `batchSetAssetMetadata`.

Mise en oeuvre de la prise en charge des données spécifiques à l’application.

Mise en oeuvre de la prise en charge des indicateurs booléens pour `createTemplate`, `extendLayers` et `extractText` pour les tâches de transfert afin de contrôler le processus de traitement Photoshop (similaire aux modifications pour les transferts de fichiers supplémentaires).

Mise en oeuvre des opérations `setImageMaps` et `setZoomTargets`.

Mise en oeuvre des opérations `ViewerPreset`. Les types reconnus sont les suivants :

* `VideoPlayer` (La vidéo publie uniquement ces visionneuses.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Les habillages des visionneuses prennent en charge deux paramètres : `skinFg` et `skinBg`. Le code principal effectue tout le traitement nécessaire pour maintenir la compatibilité ascendante.

Mise en oeuvre de l&#39;opération `getAssociatedAssets`.

Type de tâche `ReprocessAssets` Ajouté pour permettre le retraitement des fichiers source Principaux précédemment téléchargés, y compris l’extraction de fichiers PDF et la réoptimisation des images.

Le type de champ `PropertySetType` a été renommé `propertyType`. Cela affecte le paramètre `createPropertySetType` et la réponse `getPropertySetType/getPropertySetTypes`.

Mise en oeuvre de l&#39;opération `batchSetImageFields` pour prendre en charge la définition des données utilisateur d&#39;image et d&#39;autres champs d&#39;image modifiables.

47 Champ fileSize Ajouté à divers types d’informations sur les ressources :

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

Mise en oeuvre de l&#39;opération `getActivePublishContexts`. Cette opération renvoie un tableau de noms de contexte de publication avec des serveurs de publication principaux pour la société spécifiée. Les noms de contexte de publication actuels sont :

* `ImageServing`
* `ImageRendering`
* `Video`

Mise en oeuvre de l&#39;opération `getSearchStrings`. Elle renvoie un tableau de chaînes de recherche pour la ressource donnée.

Paramètres régionaux Ajoutés pour les tâches et mécanisme permettant de définir les paramètres régionaux pour les opérations d’API. La chaîne de paramètres régionaux doit être formatée sous la forme `<language_code>[-<country_code>]`. Le code de langue est un code à deux lettres minuscule, comme indiqué par ISO-639, et le code de pays facultatif est un code à deux lettres majuscule, comme spécifié par ISO-3166.

Paramètre régional facultatif Ajouté dans l’en-tête SOAP `authHeader` pour définir le paramètre régional associé aux opérations d’API. Si ce paramètre n&#39;est pas présent, l&#39;en-tête HTTP `Accept-Language` est utilisé. Si cet en-tête n&#39;est pas non plus présent, les paramètres régionaux par défaut du serveur IPS sont utilisés.

Prise en charge Ajoutée de l’obtention et de la définition des champs de métadonnées fortement typés.

Mise en oeuvre de la prise en charge des en-têtes SOAP et HTTP pour le contrôle des réponses gzip.

Indicateur `gzipResponse` Ajouté à `authHeader`. S&#39;il n&#39;est pas présent, l&#39;API vérifie également l&#39;en-tête HTTP `Accept-Encoding`.

Prise en charge Ajoutée de searchAssets pour les conditions de champ de métadonnées fortement typées.

* Pour tous les types de champs, la valeur peut être transmise avec un opérateur de comparaison de chaînes ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`).
* Pour les champs booléens, `boolVal` peut être transmis avec l&#39;`Equals` op.
* Pour les champs Int, `longVal` peut être transmis avec un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minLong/maxLong` peut être transmis avec une plage numérique ( `Between, NotBetween`).
* Pour les champs flottants, `doubleVal` peut être transmis avec un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minDouble/maxDouble` peut être transmis avec une plage numérique ( `Between, NotBetween`).
* Pour les champs Date, vous pouvez transmettre `dateVal` avec un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou vous pouvez transmettre minDate/maxDate avec une plage numérique ( `Between, NotBetween`).

Description Ajoutée, `jobSubType` et `originalJobName` champs de type `JobLog`.

* `originalJobName` est le nom de la tâche envoyée à  `submitJob` (sans suffixes d’unicité ni noms de tâche consécutifs).
* `jobSubType` n’est actuellement utilisée que par  `ImageServingPublishJob` les tâches (où il s’agit d’une des  `full`,  `increment, fullwithsearch,` ou  `fulloverride`des).
* `description` est actuellement une chaîne vide pour tous les types de tâche, mais contiendra éventuellement des informations de tâche récapitulatives, telles que le chemin d’accès au téléchargement.

En outre, les champs suivants ne sont pas inclus avec les champs `getJobLogs` et `getJobLogDetails`. Dans les versions antérieures, ils n&#39;étaient disponibles qu&#39;avec `getJobLogDetails`.

* `endDate` (si la tâche est terminée).
* `fileDuplicateCount` (auparavant, il était toujours  `0` avec  `getJobLogs`)
* `fileUpdateCount` (auparavant, il était toujours  `0` accompagné  `getJobLogs` et inclus dans  `fileSuccessCount`; elle est maintenant divisée en champs distincts).

Champ assetHandle Ajouté de type `JobLogDetail`.

Paramètre de description facultatif Ajouté à `submitJob`. Elle est transmise pour récupération dans `getScheduledJobs`, `getActiveJobs` et `getJobLogs`.

Déconseillé au champ du système SKU. Le champ est ignoré s’il est transmis sous la forme `SystemFieldCondition` à `searchAssets`.

Filtre `excludeAssetTypeArray` Ajouté sur `searchAssets`.

Type `MaskInfo` Ajouté à `Asset`.

Nouveaux types d&#39;actifs Ajoutés pour la gestion par IPS :

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
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>Document Microsoft Word pour les fichiers se terminant par .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>Document Microsoft Excel pour les fichiers se terminant par .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>Document Microsoft PowerPoint pour les fichiers se terminant par .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>fichier RTF pour les fichiers téléchargés se terminant par .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ajout d’options supplémentaires à `UploadDirectoryJob` et `UploadUrlsJob` pour contrôler le traitement des fichiers Postscript, Illustrator et PDF indépendamment. Tous les emplois existants fourniront les paramètres nécessaires à chacun des trois pipelines de transformation afin qu&#39;ils fonctionnent exactement comme aujourd&#39;hui. Le bloc `PostScriptOptions` d&#39;origine est utilisé pour définir le traitement des fichiers Illustrator et EPS/PS. Vous pouvez éventuellement fournir des blocs d&#39;options de fichier spécifiques pour spécifier le traitement. La liste des modifications comprend :

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processus </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Aucun </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Pixelliser  </span>(par défaut) </p> </li> 
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
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processus </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Aucun </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Pixelliser  </span> (par défaut) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Ne gérez que la ressource et ne créez pas de dérivés au moment du téléchargement. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Générer le fichier dans une image à la résolution et à l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> résolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entier&gt; </span> </p> </td> 
   <td colname="col4"> <p>Pixellisation de la résolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Espace colorimétrique </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espace colorimétrique de la cible pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha  </span> </p> <p>Facultatif. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Cet effet est affecté lors de la pixellisation du fichier dans une image. Crée un arrière-plan transparent si le fichier d’origine est défini de cette façon pour créer des logos superposés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> Options PDFO  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processus </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Aucun </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Pixelliser  </span> (par défaut) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Ne gérez que la ressource et ne créez pas de dérivés au moment du téléchargement. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Générer le fichier dans une image à la résolution et à l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> résolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entier&gt; </span> </p> </td> 
   <td colname="col4"> <p>Pixellisation de la résolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Espace colorimétrique </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espace colorimétrique de la cible pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit s’il faut combiner un PDF de plusieurs pages dans un catalogue électronique après le rendu (la valeur par défaut est true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit si les mots du PDF sont extraits dans la base de données pour être ensuite fournis à un serveur de recherche (la valeur par défaut est false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez également requête à partir de `getScheduledJobs`.

Modification de la propriété de configuration `webservice.gzip.response` afin de prendre l’une des valeurs suivantes :

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
