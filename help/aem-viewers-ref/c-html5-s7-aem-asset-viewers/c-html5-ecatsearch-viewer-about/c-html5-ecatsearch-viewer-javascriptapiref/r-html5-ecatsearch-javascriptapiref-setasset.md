---
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: ab078f32-c523-4b6c-a0d6-45dd2af35b36
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse de vidéos.

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier </span></span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nouvel ID de fichier ou visionneuse d’images explicites avec les modificateurs facultatifs de diffusion d’images ajoutés après <span class="codeph"> ? </span>. </p> <p> Les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit une nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après [!DNL `init()`]. S’il est appelé après [!DNL `init()`], le lecteur permute la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Référence unique à une visionneuse d’images définie dans un catalogue :

```
 <instance>.setAsset("Viewers/Pluralist")
```

Visionneuse d’images explicite, avec pages précombinées :

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Visionneuse d’images explicite, avec des images de page individuelles :

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Modificateur d’accentuation ajouté à toutes les images de la visionneuse :

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

