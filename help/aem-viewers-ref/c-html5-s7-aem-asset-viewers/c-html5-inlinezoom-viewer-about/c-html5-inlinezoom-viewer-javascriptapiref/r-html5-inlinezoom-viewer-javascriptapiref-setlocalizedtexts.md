---
title: setLocalizedTexts
description: JavaScript référence de l’API pour la visionneuse de zoom intégrée.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: a0d602f5-e698-4dad-af95-70ef5ef88af6
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

JavaScript référence de l’API pour la visionneuse de zoom intégrée.

` setLocalizedTexts( *`Informations de localisation`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Informations de </span> localisation </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">{ Object </span>} Objet JSON avec données de localisation. </p> <p>Pour plus d’informations, voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localisation des éléments </a> de l’interface utilisateur. </p> <p>Voir le Guide<i> de l’utilisateur </i>du Kit de développement logiciel (SDK) de la visionneuse et l’exemple pour plus d’informations sur le contenu de l’objet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définit les valeurs de SYMBOL de localisation pour un ou plusieurs paramètres régionaux. Ce paramètre doit être appelé avant `init()`.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```
