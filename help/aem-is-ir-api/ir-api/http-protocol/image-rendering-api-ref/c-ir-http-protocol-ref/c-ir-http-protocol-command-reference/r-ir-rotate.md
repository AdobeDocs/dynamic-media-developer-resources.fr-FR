---
title: rotation
description: Angle de rotation du matériau. Définit l’angle de rotation des matériaux.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# rotation{#rotate}

Angle de rotation du matériau. Définit l’angle de rotation des matériaux.

` rotate= *`angle`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> angle </span> </p> </td> 
  <td class="stentry"> <p>Angle de rotation en degrés (réel). </p> </td> 
 </tr> 
</table>

Faire pivoter les matériaux de texture reproductibles (à l’exclusion des papiers peints) par multiples de 45° lorsqu’ils sont appliqués à des objets plats ou plans.

Faites pivoter les matériaux de texture reproductibles selon des angles arbitraires lorsqu’ils sont appliqués aux objets Flowline et Sketch.

Faire pivoter les matériaux de décalcomanie selon des angles arbitraires.

Les angles positifs tournent dans le sens des aiguilles d’une montre. La texture ou l’autocollant est tourné autour du point d’ancrage ( `anchor=`) ; le point d’ancrage reste aligné avec l’origine de l’objet cible.

## Propriétés {#section-ad4d07897ca24f63af1a4062f8618e36}

Attribut matériel. Ignoré par la couleur unie, le papier peint, l’armoire et les matériaux de traitement des fenêtres. *`angle`* Doit être un multiple de 45 pour les textures répétables, sauf s’il est appliqué à des objets Flowline ou Sketch.

## Par défaut {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, sans rotation.

## Voir aussi {#section-f73c00e9368b478dac1fd15bb4367a12}

[ancre=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
