---
description: Angle de rotation du matériau. Définit l'angle de rotation des matériaux.
solution: Experience Manager
title: rotation
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 6%

---


# rotate{#rotate}

Angle de rotation du matériau. Définit l&#39;angle de rotation des matériaux.

` rotate= *`Angle`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Angle </span> </p> </td> 
  <td class="stentry"> <p>Angle de rotation en degrés (réel). </p> </td> 
 </tr> 
</table>

Faire pivoter les matériaux de texture répétables (à l&#39;exclusion des papiers peints) par des multiples de 45 degrés lorsqu&#39;ils sont appliqués aux objets plats ou aux objets plan.

Faire pivoter les matériaux de texture répétables selon des angles arbitraires lorsqu&#39;ils sont appliqués aux objets Flowline et Sketch.

Faire pivoter les matériaux de décomposition par angles arbitraires.

Les angles positifs pivotent dans le sens des aiguilles d&#39;une montre. La texture ou la décale est pivotée autour du point d&#39;ancrage ( `anchor=`); le point d’ancrage reste aligné sur l’origine de l’objet cible.

## Propriétés {#section-ad4d07897ca24f63af1a4062f8618e36}

Attribut de matériau. Ignoré par les matériaux de traitement des couleurs solides, du papier peint, de l&#39;armoire et des fenêtres. *`angle`* doit être un multiple de 45 pour les textures répétables, sauf s&#39;il est appliqué aux objets de flux ou d&#39;esquisse.

## Par défaut {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sans rotation.

## Voir aussi {#section-f73c00e9368b478dac1fd15bb4367a12}

[ancrage=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
