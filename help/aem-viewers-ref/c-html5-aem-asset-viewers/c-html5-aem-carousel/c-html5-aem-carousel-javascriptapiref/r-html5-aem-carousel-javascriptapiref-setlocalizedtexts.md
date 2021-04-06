---
description: Référence de l’API JavaScript pour Carousel Viewer.
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media Classic, Visionneuses, SDK/API, Bannières de carrousel
role: Développeur, Professionnel
exl-id: 8ffb8960-187a-43ab-8081-7dfd95d4c75d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

Référence de l’API JavaScript pour Carousel Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

Définit les valeurs SYMBOL de localisation pour un ou plusieurs paramètres régionaux. Ce paramètre doit être appelé avant `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Objet</span>} JSON avec des données de localisation. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> Localisation des éléments de l’interface utilisateur</a> pour plus d’informations. </p> <p>Voir également le <i>Guide de l’utilisateur du kit de développement logiciel de visionneuse</i> et l’exemple pour plus d’informations sur le contenu de l’objet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```
