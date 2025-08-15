---
title: setLocalizedTexts
description: JavaScript référence de l’API pour la visionneuse de supports variés.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 19bc61be-4321-434a-ae2c-4576c7799c0a
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

JavaScript référence de l’API pour la visionneuse de supports variés.

` setLocalizedTexts( *`Informations de localisation`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Informations de</span> localisation </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">{ object</span>} Objet JSON avec données de localisation. </p> <p>Pour plus d’informations, voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localisation des éléments</a> de l’interface utilisateur. </p> <p>Consultez également le Guide<i> de l’utilisateur </i>du Kit de développement logiciel (SDK) de la visionneuse et l’exemple pour plus d’informations sur le contenu de l’objet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit les valeurs de SYMBOL de localisation pour un ou plusieurs paramètres régionaux. Ce paramètre doit être appelé avant `init()`.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
