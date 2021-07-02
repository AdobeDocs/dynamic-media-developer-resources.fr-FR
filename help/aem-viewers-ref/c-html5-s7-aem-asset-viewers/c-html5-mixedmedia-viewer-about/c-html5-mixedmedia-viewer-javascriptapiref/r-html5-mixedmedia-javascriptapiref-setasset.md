---
description: Référence de l’API JavaScript pour la visionneuse de supports variés.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse de supports variés.

` setAsset( *`asset`*[,data]))`

Définit la nouvelle ressource et les données de ressource supplémentaires facultatives. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, la visionneuse échange la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`asset`*`  - {  `String`} nouvel identifiant de ressource ou jeu de médias mixtes explicite, avec les modificateurs de diffusion d’images facultatifs ajoutés après  `?`.

Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

`*`data`*`  - {  `JSON`} emplacement du nouveau fichier de sous-titres.

Si elle n’est pas spécifiée, le bouton de légende n’est pas visible dans l’interface utilisateur. Les sous-titres spécifiés avec ce paramètre s’appliquent à la vidéo qui apparaît en premier dans la visionneuse de supports variés ; les vidéos suivantes sont lues sans légende. Cette visionneuse prend en charge les identifiants de composant suivants :

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Identifiant du composant </p> </th> 
   <th colname="col2" class="entry"> <p>Nom de classe du composant SDK de visionneuse </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage  </span> </p> </td> 
   <td colname="col2"> <p>Image à afficher sur la première image avant le début de la lecture de la vidéo. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> caption  </span> </p> </td> 
   <td colname="col2"> <p> Emplacement du nouveau fichier de sous-titres. </p> <p>Si elle n’est pas spécifiée, le bouton de légende n’est pas visible dans l’interface utilisateur. Les sous-titres spécifiés avec ce paramètre s’appliquent à la vidéo qui arrive en premier dans la visionneuse de médias. Les vidéos suivantes sont lues sans légende. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Référence de visionneuse de médias uniques :

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Visionneuse de médias explicite :

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Modificateur d’accentuation ajouté à toutes les images de la visionneuse :

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
