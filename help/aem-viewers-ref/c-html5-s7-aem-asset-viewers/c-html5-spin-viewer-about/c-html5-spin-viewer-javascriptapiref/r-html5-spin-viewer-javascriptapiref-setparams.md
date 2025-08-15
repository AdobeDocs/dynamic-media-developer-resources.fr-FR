---
title: setParams
description: JavaScript référence de l’API pour la visionneuse à 360°.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 61d5b791-12bd-444a-add1-5537c71881fe
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setParams{#setparams}

JavaScript référence de l’API pour la visionneuse à 360°.

` setParams( *`paramètres`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"></span> paramètres </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">{string}</span> paires de paramètres name=value séparées par <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit un ou plusieurs paramètres sur une valeur donnée. La syntaxe de l’argument de méthode est identique à une chaîne de requête d’URL. Autrement dit, il représente les paires nom=valeur séparées par `&`. Comme dans une chaîne de requête, les noms et les valeurs sont codés en pourcentage au moyen du codage UTF8. Avant d’appeler `init()`, ce paramètre doit être appelé.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises `config` avec l’objet JSON au constructeur.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("SpinView.zoomstep=2,3&SpinView.iscommand=op_sharpen%3d1")
```
