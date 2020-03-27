---
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: c1bc5271-2444-4f6b-8bed-5df88ecd59f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

Référence de l’API JavaScript pour la visionneuse de vidéos.

` setParam( *`name, value`*)`

Définit le paramètre de la visionneuse sur une valeur spécifiée. Le paramètre est soit une option de configuration spécifique au lecteur de contenu, soit un modificateur de kit de développement logiciel. Ce paramètre est appelé auparavant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse ont été transmises avec l’objet `config` JSON au constructeur.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

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

