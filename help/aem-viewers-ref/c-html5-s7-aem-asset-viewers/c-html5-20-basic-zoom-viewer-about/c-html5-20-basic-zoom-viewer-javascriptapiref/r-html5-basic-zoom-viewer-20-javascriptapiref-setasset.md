---
title: setAsset
description: Référence de l’API JavaScript pour la visionneuse Zoom de base.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 71525aac-b8ca-4f5a-a770-268857ddae4f
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 2%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse Zoom de base.

` setAsset( *`ressource`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ressource </span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nouvel identifiant de ressource, avec des modificateurs IS facultatifs ajoutés après « ? » </p> <p> Les images qui utilisent le rendu d’image (IR) ou le contenu créé par l’utilisateur (UGC) ne sont pas pris en charge par cette visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après la `init()`. Si elle est appelée après `init()`, la visionneuse permute la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Référence d’image unique :

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Modificateur d’accentuation ajouté à toutes les images de la visionneuse :

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```
