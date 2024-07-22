---
title: setAsset
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 1%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse de vidéos.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ressource </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Chaîne </span> nouvel identifiant de ressource, jeu d’images explicite ou jeu d’images explicites avec des modificateurs de diffusion d’images spécifiques au cadre, avec les modificateurs de diffusion d’images globaux facultatifs ajoutés après "?". </p> <p> Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, la visionneuse échange la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Référence d’image unique comme suit :

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Référence unique à une visionneuse d’images définie dans un catalogue comme suit :

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Visionneuse d’images explicite comme suit :

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Visionneuse d’images explicite avec des modificateurs de diffusion d’images spécifiques au cadre comme suit :

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificateur d’accentuation ajouté à toutes les images de la visionneuse comme suit :

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
