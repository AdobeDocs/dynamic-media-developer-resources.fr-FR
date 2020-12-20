---
description: Référence de l’API JavaScript pour Carousel Viewer.
seo-description: Référence de l’API JavaScript pour Carousel Viewer.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 87f16ea9-0267-4114-9aeb-a68fdb616a88
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 3%

---


# setParam{#setparam}

Référence de l’API JavaScript pour Carousel Viewer.

` setParam( *`name, value`*)`

Définit le paramètre de visionneuse sur une valeur spécifiée. Le paramètre est soit une option de configuration spécifique au lecteur, soit un modificateur de kit de développement logiciel. Ce paramètre est appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse ont été transmises avec l’objet JSON `config` au constructeur.

Voir aussi [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## Paramètres {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```

