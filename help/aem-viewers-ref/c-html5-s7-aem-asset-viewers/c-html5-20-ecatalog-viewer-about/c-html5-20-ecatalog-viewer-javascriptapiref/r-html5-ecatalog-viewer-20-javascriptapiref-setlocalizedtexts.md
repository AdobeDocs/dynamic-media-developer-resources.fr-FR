---
title: setLocalizedTexts
description: JavaScript référence de l’API pour la visionneuse vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 89d6231d-8063-435f-864e-c352287e4764
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

JavaScript référence de l’API pour la visionneuse vidéo.

` setLocalizedTexts( *`Informations de localisation`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Informations de</span> localisation </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">{ object</span>} Objet JSON avec données de localisation. </p> <p>Pour plus d’informations, voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localisation des éléments</a> de l’interface utilisateur. </p> <p>Consultez également le Guide<i> de l’utilisateur </i>du Kit de développement logiciel (SDK) de la visionneuse et l’exemple pour plus d’informations sur le contenu de l’objet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit les valeurs de SYMBOL de localisation pour un ou plusieurs paramètres régionaux. Ce paramètre doit être appelé avant `init()`.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
