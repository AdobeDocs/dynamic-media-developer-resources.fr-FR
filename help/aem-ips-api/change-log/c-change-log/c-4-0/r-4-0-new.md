---
description: Décrit les modifications nouvelles et mises en oeuvre pour l'API IPS v4.0.
seo-description: Décrit les modifications nouvelles et mises en oeuvre pour l'API IPS v4.0.
seo-title: Nouvelles ajouts et modifications
solution: Experience Manager
title: Nouvelles ajouts et modifications
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Nouvelles ajouts et modifications{#new-additions-and-changes}

Décrit les modifications nouvelles et mises en oeuvre pour l&#39;API IPS v4.0.

Mise en oeuvre de versions d’API côte à côte avec des WSDL et des   distincts.

* Versions d’API précédentes : `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Version SPS 4.0 : `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Ajout `PostScriptOptions/alpha` d’un champ.

Ajout `VideoRootUrl` et `SwfRootUrl` des propriétés pour l’ `getProperty` opération.

Ajout de paramètres facultatifs `appName` et `appVersion` pour effectuer `authHeader` le suivi de l’application d’appel. Ajout de la connexion à `ipsApiService.log`.

Ajout d’un `serviceUrl` paramètre facultatif à la servlet de génération WSDL. Ceci est particulièrement utile pour les proxies de débogage. Par exemple: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Opération `getZipEntries` mise en oeuvre.

Mise en oeuvre de plages de recherche et de valeurs de comparaison saisies pour les conditions de champ système.

Ajout d’une constante de chaîne de type `'Asset'` de ressource, principalement pour autoriser les champs de métadonnées interactifs.

Mise en oeuvre du `trashState` paramètre pour `searchAssets`.

Opération `getAssetPublishHistory` mise en oeuvre.

Ajout de l’en-tête `faultHttpStatusCode` SOAP facultatif pour activer la gestion des erreurs dans Flex. Pour Flex, utilisez `<faultHttpStatusCode>200</faultHttpStatusCode>`. Le code d’état par défaut pour les réponses d’erreur est `500 (Internal Server Error)`.

Ajout d’opérations de restauration des fichiers de la corbeille et des fichiers vides de la corbeille.

Mise en oeuvre des opérations CRUD.

Ajout de l’indicateur activé au `ImageMap` type et `saveImageMap` à l’opération.

Ajout de la prise en charge des tâches Optimiser les fichiers restants.

Ajout `setAssetsPublishState` pour les mises à jour d’état de publication en bloc.

Added `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Opération déconseillée `saveMetadataField` en faveur de nouvelles `createMetadataField` et `updateMetadataField` opérations.

Opération de suppression `deleteAssetsParam` par lot implémentée.

Mise en oeuvre de l’opération `moveAssetsParam` de déplacement par lot.

Opération `deleteMetadataField` mise en oeuvre.

Mise en oeuvre `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` des opérations.

Implemented `getAssetCounts`.

Ajout de la prise en charge de `setImageSetMembers` l’inclusion de `RenderSet` membres dans `ImageSet` les ressources.

Ajout de `replaceImage` l’opération.

Ajout de `copyImage` l’opération.

Ajout `setUrlModifier` d’une opération et de `urlModifier/urlPostApplyModifier` champs pour `LayerViewInfo`, `TemplateInfo`et `WatermarkInfo`.

Ajout de `createDerivedAsset` l’opération. Actuellement, il `ownerHandle` doit référencer un fichier d’image et le type peut être `AdjustedView` ou `LayerView`.

Ajout de `createTemplate` l’opération. Actuellement, il est possible de l’appeler pour créer des ressources de modèle ou de filigrane.

Paramètres de  IPS, `CompanySettings`, portés vers l&#39;API des services Web.

Ajout de l’indicateur `excludeByproducts` de filtre au `searchAssets` fonctionnement. La définition de cet indicateur sur true exécute `PSDlayer` les images et les images pixellisées au format PDF.

Ajout de `getGenerationInfo` l’opération.

Ajout du nom `SystemMessage` de propriété à `getProperty` l’opération.

Modification de certaines constantes de chaîne de type de ressource pour qu’elles correspondent aux champs Informations sur le fichier correspondants.

* WordDoc : Word
* ExcelDoc : Excel
* PowerPointDoc : PowerPoint
* RTFDoc : Rtf

Modification du format de résultat des opérations par lot pour résumer la réussite, les avertissements et les erreurs.

Mise en oeuvre de l’opération `batchSetAssetMetadata` de métadonnées par lot.

Mise en oeuvre de la prise en charge des données spécifiques à l’application.

Mise en oeuvre de la prise en charge des indicateurs booléens pour `createTemplate`, `extendLayers`et `extractText` les tâches de téléchargement afin de contrôler le processus de traitement Photoshop (comme les modifications pour l’ajout de téléchargements de fichiers).

Mise en oeuvre `setImageMaps` et `setZoomTargets` opérations.

Opérations `ViewerPreset` mises en oeuvre. Les types reconnus sont les suivants :

* `VideoPlayer` (La vidéo publie uniquement ces visionneuses.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Les habillages de la visionneuse prennent en charge deux paramètres : `skinFg` et `skinBg`. Le code principal effectue tout le traitement nécessaire pour maintenir la compatibilité ascendante.

Opération `getAssociatedAssets` mise en oeuvre.

Ajout du type de `ReprocessAssets` tâche pour permettre le retraitement des fichiers originaux précédemment téléchargés, y compris la récupération des fichiers PDF et la réoptimisation des images.

Le type de `PropertySetType` champ a été renommé `propertyType`. Cela affecte le `createPropertySetType` paramètre et la `getPropertySetType/getPropertySetTypes` réponse.

Mise en oeuvre `batchSetImageFields` d’une opération de prise en charge de la définition des données utilisateur de l’image et d’autres champs d’image modifiables.

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

Opération `getActivePublishContexts` mise en oeuvre. Cette opération renvoie un tableau de noms de contexte de publication avec des serveurs de publication actifs pour le  spécifié. Les noms de contexte de publication actuels sont :

* `ImageServing`
* `ImageRendering`
* `Video`

Opération `getSearchStrings` mise en oeuvre. Elle renvoie un tableau de chaînes de recherche pour la ressource donnée.

Ajout de paramètres régionaux pour les tâches et d’un mécanisme pour définir les paramètres régionaux pour les opérations de l’API. La chaîne de paramètres régionaux doit être formatée `<language_code>[-<country_code>]`. Le code de langue est un code à deux lettres minuscule, spécifié par ISO-639, et le code de pays facultatif est un code à deux lettres majuscule, spécifié par ISO-3166.

Ajout d’un paramètre régional facultatif à l’en-tête `authHeader` SOAP pour définir le paramètre régional des opérations de l’API. Si ce paramètre n’est pas présent, l’en-tête HTTP `Accept-Language` sera utilisé. Si cet en-tête n&#39;est pas non plus présent, les paramètres régionaux par défaut du serveur IPS sont utilisés.

Ajout de la prise en charge de la fonction d’obtention/définition pour les champs de métadonnées fortement tapés.

Mise en oeuvre de la prise en charge des en-têtes SOAP et HTTP pour le contrôle des réponses gzip.

Ajout `gzipResponse` d’un indicateur à `authHeader`. S&#39;il n&#39;est pas présent, l&#39;API vérifie également l&#39;en-tête HTTP `Accept-Encoding` .

Ajout de la prise en charge de searchAssets pour les conditions de champ de métadonnées fortement tapées.

* Pour tous les types de champs, la valeur peut être transmise avec un opérateur de comparaison de chaînes ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Pour les champs booléens, `boolVal` il est possible de transmettre la variable `Equals` op.
* Pour les champs Int, `longVal` vous pouvez passer par un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minLong/maxLong` passer par une plage numérique ( `Between, NotBetween`).
* Pour les champs flottants, `doubleVal` vous pouvez passer par un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou `minDouble/maxDouble` passer par une plage numérique ( `Between, NotBetween`).
* Pour les champs Date, vous pouvez transmettre `dateVal` un opérateur de comparaison numérique ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) ou transmettre minDate/maxDate avec une plage numérique ( `Between, NotBetween`).

Ajout d’une description, `jobSubType`et de `originalJobName` champs à `JobLog` saisir.

* `originalJobName` est le nom de la tâche envoyée à `submitJob` (sans suffixe d’unicité ni nom de tâche ultérieur).
* `jobSubType` est actuellement utilisée uniquement par `ImageServingPublishJob` les tâches (où il s’agit d’une `full`, `increment, fullwithsearch,` ou `fulloverride`).
* `description` est actuellement une chaîne vide pour tous les types de tâche, mais contiendra éventuellement des informations de tâche récapitulatives, telles que le chemin d’accès au téléchargement.

En outre, les champs suivants ne sont pas inclus avec les deux `getJobLogs` et `getJobLogDetails`. Dans les versions précédentes, ils n&#39;étaient disponibles qu&#39;avec `getJobLogDetails`.

* `endDate` (si la tâche est terminée).
* `fileDuplicateCount` (auparavant, c&#39;était toujours `0` avec `getJobLogs`)
* `fileUpdateCount` (précédemment, était toujours `0` avec `getJobLogs` et inclus dans `fileSuccessCount`; il est maintenant divisé en champs distincts).

Ajout du champ assetHandle à `JobLogDetail` saisir.

Ajout d’un paramètre de description facultatif à `submitJob`. Elle est transmise pour récupération dans `getScheduledJobs`, `getActiveJobs`et `getJobLogs`.

Le champ du système SKU a été obsolète. Le champ est ignoré s’il est transmis sous la forme d’un `SystemFieldCondition` à `searchAssets`.

Ajout d’un `excludeAssetTypeArray` filtre à `searchAssets`.

Ajout d’un `MaskInfo` type à `Asset`.

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
   <td colname="col1"> <p> <span class="codeph"> Postscript </span> </p> </td> 
   <td colname="col2"> <p>Fichiers EPS et PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft Word pour les fichiers se terminant par .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft Excel pour les fichiers se terminant par .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft PowerPoint pour les fichiers se terminant par .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>fichier RTF pour les fichiers téléchargés se terminant par .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ajout d’options supplémentaires pour `UploadDirectoryJob` et `UploadUrlsJob` pour contrôler le traitement indépendant des fichiers Postscript, Illustrator et PDF. Toutes les tâches existantes fourniront les paramètres nécessaires à chacun des trois pipelines de traitement afin qu&#39;ils fonctionnent exactement comme aujourd&#39;hui. Le `PostScriptOptions` bloc d’origine permet de définir le traitement des fichiers Illustrator et EPS/PS. Si vous le souhaitez, des blocs d’options de fichier spécifiques peuvent être fournis pour spécifier le traitement. Le de modifications inclut :

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
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gérez uniquement le fichier et ne créez aucun produit dérivé au moment du téléchargement. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Générer le fichier EPS et PostScript dans une image à la résolution et à l’espace colorimétrique prescrits. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Facultatif. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Prend effet lors de la pixellisation du fichier dans une image. Il créera un arrière-plan transparent si le fichier d’origine est défini de cette façon pour l’incrustation de logos. </p> </td> 
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
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gérez uniquement le fichier et ne créez aucun produit dérivé au moment du téléchargement. </p> </li> 
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
   <td colname="col4"> <p>Espace colorimétrique  pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Facultatif. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Cela a une incidence sur la pixellisation du fichier dans une image. Crée un arrière-plan transparent si le fichier d’origine est défini de cette manière pour la création de logos superposés. </p> </td> 
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
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gérez uniquement le fichier et ne créez aucun produit dérivé au moment du téléchargement. </p> </li> 
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
   <td colname="col4"> <p>Espace colorimétrique  pour le rendu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit si vous souhaitez combiner un PDF de plusieurs pages dans un catalogue électronique après le rendu (la valeur par défaut est true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Définit si les mots du PDF sont extraits dans la base de données pour être ensuite fournis à un serveur de recherche (la valeur par défaut est false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez également  à partir de `getScheduledJobs`.

Modification de la propriété `webservice.gzip.response` de configuration pour prendre l’une des valeurs suivantes :

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
   <td colname="col2"> <p>Gzip si authHeader/gzipResponse a la valeur true, ou si aucun en-tête gzipResponse n’est présent et que l’en-tête HTTP Accept-Encoding inclut gzip. (Par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toujours </span> </p> </td> 
   <td colname="col2"> <p>Toujours gzip, quelle que soit la valeur de l’en-tête. Utilisez cette valeur uniquement à des fins de débogage. </p> </td> 
  </tr> 
 </tbody> 
</table>

