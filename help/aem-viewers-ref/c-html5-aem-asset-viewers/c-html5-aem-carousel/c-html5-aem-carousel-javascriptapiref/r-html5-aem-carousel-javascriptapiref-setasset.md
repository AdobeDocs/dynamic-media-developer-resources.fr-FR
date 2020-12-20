---
description: Référence de l’API JavaScript pour Carousel Viewer.
seo-description: Référence de l’API JavaScript pour Carousel Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 770cbb87-af86-48dc-88a0-e74f6716f545
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---


# setAsset{#setasset}

Référence de l’API JavaScript pour Carousel Viewer.

` setAsset( *`asset`*)`

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, le lecteur permute la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> élément</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Chaîne</span>} nouvel ID de ressource. </p> <p>Cette visionneuse ne prend pas en charge les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Référence d’image unique :

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```

