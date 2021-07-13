---
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse de vidéos.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ressource  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Chaîne </span>} nouvel identifiant de ressource, jeu d’images explicite ou jeu d’images explicites avec des modificateurs de diffusion d’images spécifiques au cadre, avec des modificateurs de diffusion d’images globaux facultatifs ajoutés après "?". </p> <p> Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, la visionneuse échange la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Référence d’image unique :

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Référence unique à une visionneuse d’images définie dans un catalogue :

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Visionneuse d’images explicite :

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Visionneuse d’images explicite avec modificateurs de diffusion d’images spécifiques au cadre :

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificateur d’accentuation ajouté à toutes les images de la visionneuse :

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
