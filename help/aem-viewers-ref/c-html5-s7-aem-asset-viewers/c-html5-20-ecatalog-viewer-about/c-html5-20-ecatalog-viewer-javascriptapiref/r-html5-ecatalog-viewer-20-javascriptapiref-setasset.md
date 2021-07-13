---
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visionneuses,SDK/API,eCatalog
role: Developer,User
exl-id: 04b6bf4d-5c42-49e9-b585-de75ebf6c89f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse de vidéos.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ressource  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Chaîne </span>} nouvel ID de ressource ou jeu d’images explicites avec des modificateurs de diffusion d’images facultatifs ajoutés après <span class="codeph"> ? </span>. </p> <p> Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit une nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, la visionneuse échange la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Référence unique à une visionneuse d’images définie dans un catalogue :

```
 <instance>.setAsset("Viewers/Pluralist")
```

Visionneuse d’images explicite, avec pages pré-combinées :

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
