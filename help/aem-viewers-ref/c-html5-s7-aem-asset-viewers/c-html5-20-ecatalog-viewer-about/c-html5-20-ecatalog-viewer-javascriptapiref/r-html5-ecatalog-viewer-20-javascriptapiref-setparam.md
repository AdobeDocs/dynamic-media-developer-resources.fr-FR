---
title: setParam
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 781982f6-488d-452c-8168-604c708ae6ce
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique.

` setParam( *`nom, valeur`*)`

Définit le paramètre de visionneuse sur une valeur spécifiée. Le paramètre est une option de configuration spécifique à la visionneuse ou un modificateur de kit de développement logiciel. Ce paramètre est appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec `config` objet JSON au constructeur .

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} nom </span> paramètre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valeur <span class="varname"> </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} valeur </span> du paramètre . La valeur ne peut pas être codée en pourcentage. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
