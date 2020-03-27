---
description: Référence de l’API JavaScript pour la visionneuse Fenêtre déroulante.
seo-description: Référence de l’API JavaScript pour la visionneuse Fenêtre déroulante.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 0c2deb6c-f40f-47e5-a1ef-f5eb5db6ee06
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

Référence de l’API JavaScript pour la visionneuse Fenêtre déroulante.

` setParam( *`name, value`*)`

Définit le paramètre de la visionneuse sur une valeur spécifiée. Le paramètre est soit une option de configuration spécifique au lecteur de contenu, soit un modificateur de kit de développement logiciel. Ce paramètre est appelé auparavant `init()`. Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec l’objet `config` JSON au constructeur.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

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

