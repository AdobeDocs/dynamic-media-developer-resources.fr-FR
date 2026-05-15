---
title: setParam
description: Référence de l’API JavaScript pour la visionneuse à 360°.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16d1d2cd-f58f-4ac3-b89f-f2f12fee231d
TQID: 'https://experienceleague.adobe.com/R0HdN4vDg-LC6em1E3KdzQI5d4uwttBhK1sQPI77Dw8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 2%

---

# setParam{#setparam}

Référence de l’API JavaScript pour la visionneuse à 360°.

` setParam( *`nom, valeur`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> nom du paramètre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valeur <span class="varname"> </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> valeur du paramètre . La valeur ne peut pas être codée en pourcentage. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit le paramètre de visionneuse sur une valeur spécifiée. Le paramètre est une option de configuration spécifique à la visionneuse ou un modificateur de kit de développement logiciel. Ce paramètre est appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec `config` objet JSON au constructeur .

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
