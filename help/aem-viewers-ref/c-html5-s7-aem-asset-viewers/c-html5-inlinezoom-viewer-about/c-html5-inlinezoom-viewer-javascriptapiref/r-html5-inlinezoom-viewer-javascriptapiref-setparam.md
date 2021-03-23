---
description: Référence de l’API JavaScript pour la visionneuse de zoom intégrée.
seo-description: Référence de l’API JavaScript pour la visionneuse de zoom intégrée.
seo-title: setParam
solution: Experience Manager
title: setParam
uuid: 7bccf2c0-9f9a-47ac-8b53-385989e8267c
feature: Dynamic Media Classic, Visionneuses, SDK/API, Zoom intégré
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# setParam{#setparam}

Référence de l’API JavaScript pour la visionneuse de zoom intégrée.

` setParam( *`name, value`*)`

Définit le paramètre de visionneuse sur une valeur spécifiée. Le paramètre est soit une option de configuration spécifique au lecteur, soit un modificateur de kit de développement logiciel. Ce paramètre est appelé avant `init()`. Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec l’objet JSON `config` au constructeur.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> nom du paramètre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> valeur du paramètre. La valeur ne peut pas être codée en pourcentage. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

