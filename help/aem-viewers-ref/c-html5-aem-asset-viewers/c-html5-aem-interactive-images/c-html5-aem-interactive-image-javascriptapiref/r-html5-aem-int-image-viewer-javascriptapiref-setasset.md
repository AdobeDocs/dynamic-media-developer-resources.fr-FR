---
description: Référence de l’API JavaScript pour la visionneuse d’images vidéo.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic, Visionneuses, SDK/API, Images interactives
role: Développeur, Professionnel
exl-id: e5f88bc9-a880-45eb-9554-57e185937d29
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse d’images vidéo.

` setAsset( *`asset`*)`

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, le lecteur permute la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> élément</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Chaîne</span>} nouvel ID de ressource. </p> <p>Les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Référence d’image unique :

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```
