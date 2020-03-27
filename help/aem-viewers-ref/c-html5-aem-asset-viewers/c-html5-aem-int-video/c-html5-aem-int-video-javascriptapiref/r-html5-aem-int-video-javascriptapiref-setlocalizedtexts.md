---
description: Référence de l’API JavaScript pour la visionneuse de vidéos interactive.
seo-description: Référence de l’API JavaScript pour la visionneuse de vidéos interactive.
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: 11844a71-adb0-42a9-9b58-b69821070fd2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setLocalizedTexts{#setlocalizedtexts}

Référence de l’API JavaScript pour la visionneuse de vidéos interactive.

` setLocalizedTexts( *`localizationInfo`*)`

Définit  valeurs SYMBOL pour un ou plusieurs paramètres régionaux. Ce paramètre doit être appelé avant `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span></span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Objet </span>} JSON avec des données . </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> des éléments de l’interface utilisateur </a> pour plus d’informations. </p> <p>Voir également le Guide <i>de l’utilisateur du kit de développement</i> de visionneuse et l’exemple pour plus d’informations sur le contenu de l’objet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

