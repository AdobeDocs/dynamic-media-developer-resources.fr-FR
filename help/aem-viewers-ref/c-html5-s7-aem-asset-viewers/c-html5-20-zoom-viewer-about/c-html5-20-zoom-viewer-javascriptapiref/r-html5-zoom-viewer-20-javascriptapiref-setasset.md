---
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: f106b3d4-880e-4ba3-ae47-a005af5c0f1b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> élément  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Chaîne </span>} : nouvel identifiant de fichier, visionneuse d’images explicites ou visionneuse d’images explicites avec modificateurs de diffusion d’images spécifiques au cadre, avec les modificateurs globaux facultatifs de diffusion d’images ajoutés après "?". </p> <p> Cette visionneuse ne prend pas en charge les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content). </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, le lecteur permute la ressource au moment de l’exécution.

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

Visionneuse d’images explicites avec modificateurs de diffusion d’images spécifiques aux images :

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificateur d’accentuation ajouté à toutes les images de la visionneuse :

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```

