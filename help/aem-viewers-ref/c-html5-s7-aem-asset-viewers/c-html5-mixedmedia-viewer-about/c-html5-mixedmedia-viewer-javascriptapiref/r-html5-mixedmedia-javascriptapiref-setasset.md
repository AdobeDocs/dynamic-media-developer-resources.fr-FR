---
description: Référence de l’API JavaScript pour la visionneuse de supports variés.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---


# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse de supports variés.

` setAsset( *`asset`*[,data]))`

Définit la nouvelle ressource et les autres données de ressource facultatives. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, le lecteur permute la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`asset`*` - {  `String`} nouvel ID de fichier ou jeu de supports mixtes explicites, avec les modificateurs facultatifs de diffusion d’images ajoutés après  `?`.

Cette visionneuse ne prend pas en charge les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content).

`*`data`*` - {  `JSON`} emplacement du nouveau fichier de sous-titrage.

Si ce n’est pas le cas, le bouton de sous-titrage n’est pas visible dans l’interface utilisateur. Les légendes spécifiées avec ce paramètre s’appliquent à la vidéo qui vient en premier dans la visionneuse de supports mixtes ; les vidéos suivantes sont lues sans légende. Cette visionneuse prend en charge les ID de composant suivants :

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID de composant </p> </th> 
   <th colname="col2" class="entry"> <p>Nom de classe du composant SDK de visionneuse </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage  </span> </p> </td> 
   <td colname="col2"> <p>Image à afficher sur la première image avant la lecture des débuts de la vidéo. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> légende  </span> </p> </td> 
   <td colname="col2"> <p> Emplacement du nouveau fichier de sous-titrage. </p> <p>Si ce n’est pas le cas, le bouton de sous-titrage n’est pas visible dans l’interface utilisateur. Les légendes spécifiées avec ce paramètre s’appliquent à la vidéo qui vient en premier dans la visionneuse de supports. Les vidéos suivantes sont lues sans légende. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Référence du jeu de supports unique :

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Visionneuse de supports explicites :

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Modificateur d’accentuation ajouté à toutes les images de la visionneuse :

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

