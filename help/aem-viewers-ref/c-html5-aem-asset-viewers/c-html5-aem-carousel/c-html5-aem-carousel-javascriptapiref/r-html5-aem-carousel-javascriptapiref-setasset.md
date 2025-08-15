---
title: setAsset
description: Référence de l’API JavaScript pour la visionneuse de carrousel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: e8aaee4e-56d5-46e4-8499-d5c9a6ba5d3b
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 2%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse de carrousel.

` setAsset( *`ressource`*)`

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après la `init()`. Si elle est appelée après `init()`, la visionneuse permute la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ressource </span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nouvel ID de ressource. </p> <p>Les images qui utilisent le rendu d’image (IR) ou le contenu créé par l’utilisateur (UGC) ne sont pas pris en charge par cette visionneuse. </p> </td>
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

