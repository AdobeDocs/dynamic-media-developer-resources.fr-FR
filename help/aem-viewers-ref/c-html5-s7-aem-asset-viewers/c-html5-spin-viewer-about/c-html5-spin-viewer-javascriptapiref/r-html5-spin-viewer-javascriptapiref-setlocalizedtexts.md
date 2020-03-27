---
description: Référence de l’API JavaScript pour la visionneuse à 360°.
seo-description: Référence de l’API JavaScript pour la visionneuse à 360°.
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: bf136479-8ac8-4151-8911-377eed631aa2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedTexts{#setlocalizedtexts}

Référence de l’API JavaScript pour la visionneuse à 360°.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span></span> </p> </td> 
   <td colname="col2"> <p> Objet JSON {<span class="codeph"> Object</span>} avec données . </p> <p>Pour plus d’informations, voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> des éléments</a> de l’interface utilisateur. </p> <p>Voir également le Guide <i>de l’utilisateur du kit de développement</i> de visionneuse et l’exemple pour plus d’informations sur le contenu de l’objet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit  valeurs SYMBOL pour un ou plusieurs paramètres régionaux. Ce paramètre doit être appelé avant `init()`.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

