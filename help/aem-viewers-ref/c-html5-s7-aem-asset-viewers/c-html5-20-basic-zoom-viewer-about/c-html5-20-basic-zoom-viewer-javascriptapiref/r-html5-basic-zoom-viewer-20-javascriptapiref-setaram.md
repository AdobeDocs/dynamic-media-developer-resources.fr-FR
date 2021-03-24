---
description: Référence de l’API JavaScript pour la visionneuse de zoom de base.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic, Visionneuses, SDK/API, Zoom
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---


# setParam{#setparam}

Référence de l’API JavaScript pour la visionneuse de zoom de base.

` setParam( *`name, value`*)`

Définit le paramètre de visionneuse sur une valeur spécifiée. Le paramètre est soit une option de configuration spécifique au lecteur, soit un modificateur de kit de développement logiciel. Ce paramètre est appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse ont été transmises avec l’objet JSON `config` au constructeur.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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

