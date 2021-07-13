---
description: Angle de rotation du matériau. Définit l’angle de rotation des matériaux.
solution: Experience Manager
title: rotation
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---

# rotation{#rotate}

Angle de rotation du matériau. Définit l’angle de rotation des matériaux.

` rotate= *`Angle`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Angle </span> </p> </td> 
  <td class="stentry"> <p>Angle de rotation en degrés (réel). </p> </td> 
 </tr> 
</table>

Faire pivoter les matériaux de texture répétables (hors papiers peints) par des multiples de 45 degrés lorsqu’ils sont appliqués aux objets plats ou aux objets de plan.

Faire pivoter les matériaux de texture répétables par des angles arbitraires lorsqu’ils sont appliqués aux objets de type Flowline ou Sketch.

Faire pivoter les matériaux de décomposition par des angles arbitraires.

Les angles positifs tournent dans le sens des aiguilles d&#39;une montre. La texture ou la décomposition est pivotée autour du point d’ancrage ( `anchor=`) ; le point d’ancrage reste aligné sur l’origine de l’objet cible.

## Propriétés {#section-ad4d07897ca24f63af1a4062f8618e36}

Attribut de matière. Ignoré par les matériaux de traitement des vitres, des papiers peints et des couleurs solides. *`angle`* doit être un multiple de 45 pour les textures répétables, sauf s’il est appliqué à Flux ou à Objets d’esquisse.

## Par défaut {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sans rotation.

## Voir aussi {#section-f73c00e9368b478dac1fd15bb4367a12}

[ancrage=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
