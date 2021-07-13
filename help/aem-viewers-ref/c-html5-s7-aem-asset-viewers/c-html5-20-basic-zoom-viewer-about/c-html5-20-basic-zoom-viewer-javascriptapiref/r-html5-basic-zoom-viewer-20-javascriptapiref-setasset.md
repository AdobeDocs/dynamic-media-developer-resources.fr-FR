---
description: Référence de l’API JavaScript pour la visionneuse de zoom de base.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom
role: Developer,User
exl-id: 71525aac-b8ca-4f5a-a770-268857ddae4f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# setAsset{#setasset}

Référence de l’API JavaScript pour la visionneuse de zoom de base.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ressource</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Chaîne</span>} nouvel ID de ressource, avec les modificateurs IS facultatifs ajoutés après "?" </p> <p> Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit la nouvelle ressource. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. S’il est appelé après `init()`, la visionneuse échange la ressource au moment de l’exécution.

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
