---
title: setParam
description: Référence de l’API JavaScript pour la visionneuse d’images vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: ef307acb-2ff0-46df-a06b-8dbac2e412f9
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# setParam{#setparam}

Référence de l’API JavaScript pour la visionneuse d’images vidéo.

` setParam( *`nom, valeur`*)`

Définit le paramètre de visionneuse sur une valeur spécifiée. Le paramètre est une option de configuration spécifique à la visionneuse ou un modificateur de kit de développement logiciel. Ce paramètre est appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse ont été transmises avec `config` objet JSON au constructeur .

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Paramètres {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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
<instance>.setParam("style", "etc/dam/presets/css/html5_interactiveimage.css")
```
