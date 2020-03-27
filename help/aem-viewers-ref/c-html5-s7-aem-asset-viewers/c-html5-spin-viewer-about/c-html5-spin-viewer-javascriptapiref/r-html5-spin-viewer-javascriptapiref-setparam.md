---
description: Référence de l’API JavaScript pour la visionneuse à 360°.
seo-description: Référence de l’API JavaScript pour la visionneuse à 360°.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 5f7be1d4-28aa-497c-9067-853c227aa11a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

Référence de l’API JavaScript pour la visionneuse à 360°.

` setParam( *`name, value`*)`

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

Définit le paramètre de la visionneuse sur une valeur spécifiée. Le paramètre est soit une option de configuration spécifique au lecteur de contenu, soit un modificateur de kit de développement logiciel. Ce paramètre est appelé auparavant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec l’objet `config` JSON au constructeur.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

