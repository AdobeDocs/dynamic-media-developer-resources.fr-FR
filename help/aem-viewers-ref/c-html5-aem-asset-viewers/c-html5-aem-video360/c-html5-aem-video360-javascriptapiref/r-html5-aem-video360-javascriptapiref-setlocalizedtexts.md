---
title: setLocalizedTexts
description: Référence de l’API JavaScript pour la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b0434886-defa-47d4-9853-bfd73c64d036
TQID: 'https://experienceleague.adobe.com/oXnXBZeFmBHsA4JCdRKFaUo0TCU6g6hqXf97cz7-AHo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 69
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

Référence de l’API JavaScript pour la visionneuse Video360.

` setLocalizedTexts( *`localizationInfo`*)`

Définit les valeurs des symboles de localisation pour un ou plusieurs paramètres régionaux. Ce paramètre doit être appelé avant `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Object </span>} Objet JSON avec des données de localisation. </p> <p>Pour plus d’informations, consultez <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> section Localisation des éléments de l’interface utilisateur </a> . </p> <p>Consultez également le <i>Guide d’utilisation de la visionneuse SDK</i> et l’exemple pour plus d’informations sur le contenu de l’objet . </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
