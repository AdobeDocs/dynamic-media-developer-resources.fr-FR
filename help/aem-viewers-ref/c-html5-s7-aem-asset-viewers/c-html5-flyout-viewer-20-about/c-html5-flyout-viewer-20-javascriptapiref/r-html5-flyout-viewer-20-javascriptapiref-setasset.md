---
title: setAsset
description: Référence de l’API JavaScript pour la visionneuse déroulante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: cd66267e-7b25-4af4-b83c-f7b7f768ea8c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 1%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse déroulante.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ressource</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Chaîne</span>} nouvel identifiant de ressource, jeu d’images explicites ou jeu d’images explicites avec des modificateurs de diffusion d’images spécifiques au cadre, avec des modificateurs globaux de diffusion d’images facultatifs ajoutés après <span class="codeph"> ?</span>. </p> <p> Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, la visionneuse échange la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

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

Visionneuse d’images explicite comme suit :

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Visionneuse d’images explicite avec modificateurs de diffusion d’images spécifiques au cadre :

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificateur d’accentuation ajouté à toutes les images de la visionneuse :

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
