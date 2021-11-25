---
title: setAsset
description: Référence de l’API JavaScript pour la visionneuse panoramique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse panoramique.

`setAsset(asset)`

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, la visionneuse échange la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-javascriptapiref/r-html5-aem-panoramic-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Chaîne</span>} nouvel ID de ressource. Les images qui utilisent le rendu d’image (IR) ou le contenu généré par l’utilisateur (UGC) ne sont pas prises en charge par cette visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/PanoramicImage-Sample")
```
