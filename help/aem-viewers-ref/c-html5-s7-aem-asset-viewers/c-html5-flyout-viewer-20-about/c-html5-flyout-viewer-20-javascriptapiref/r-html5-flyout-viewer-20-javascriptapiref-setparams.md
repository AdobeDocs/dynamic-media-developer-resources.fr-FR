---
title: setParams
description: Référence de l’API JavaScript pour la visionneuse Fenêtre déroulante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: bd26292d-f9c6-4e67-8cc1-c74336d50860
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setParams{#setparams}

Référence de l’API JavaScript pour la visionneuse Fenêtre déroulante.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> paramètres </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value paires de paramètres séparées par <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit un ou plusieurs paramètres sur une valeur donnée. La syntaxe de l&#39;argument de méthode est identique à une chaîne de requête URL. En d’autres termes, il représente des paires nom=valeur séparées par des `&`. Comme dans une chaîne de requête, les noms et les valeurs sont codés en pourcentage à l’aide d’UTF8. Avant d’appeler `init()`, ce paramètre doit être appelé. Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec `config` objet JSON au constructeur .

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```
