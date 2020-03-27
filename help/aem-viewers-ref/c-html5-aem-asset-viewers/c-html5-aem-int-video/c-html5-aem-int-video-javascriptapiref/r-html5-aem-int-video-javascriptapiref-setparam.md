---
description: Référence de l’API JavaScript pour la visionneuse de vidéos interactive.
seo-description: Référence de l’API JavaScript pour la visionneuse de vidéos interactive.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: c8c40e88-530f-4af8-be9a-2e88addd6907
translation-type: tm+mt
source-git-commit: 94b8dde58cda2670f3e2f22f217599c23601e450

---


# setParam{#setparam}

Référence de l’API JavaScript pour la visionneuse de vidéos interactive.

` setParam( *`name, value`*)`

Définit le paramètre de la visionneuse sur une valeur spécifiée. Le paramètre est soit une option de configuration spécifique au lecteur de contenu, soit un modificateur de kit de développement logiciel. Ce paramètre est appelé auparavant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse ont été transmises avec l’objet `config` JSON au constructeur.

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Paramètres {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nom </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> nom du paramètre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> valeur </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> valeur du paramètre. La valeur ne peut pas être codée en pourcentage. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

