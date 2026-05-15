---
title: setParams
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: a93c14e8-d322-4630-9334-1b4413f1e443
TQID: 'https://experienceleague.adobe.com/C38zIkos57sdfGwrnK2KbVZhmJ-BCCz2w5W2ZEgnLFA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 2%

---

# setParams{#setparams}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique.

` setParams( *`params`*)`

Définit un ou plusieurs paramètres sur une valeur donnée. La syntaxe de l&#39;argument de méthode est identique à une chaîne de requête URL. En d’autres termes, il représente des paires nom=valeur séparées par des `&`. Tout comme dans une chaîne de requête, les noms et les valeurs sont codés en pourcentage à l’aide d’UTF8. Avant d’appeler `init()`, ce paramètre doit être appelé.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec `config` objet JSON au constructeur .

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> paramètres </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value paires de paramètres séparées par <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
