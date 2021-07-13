---
description: La rugosité de surface matérielle. Indique la rugosité relative de la surface du matériau.
solution: Experience Manager
title: brut
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# brut{#rough}

La rugosité de surface matérielle. Indique la rugosité relative de la surface du matériau.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Rogosité de surface (0...100 %) ou -1 pour sélectionner la rugosité par défaut. </p> </td> 
 </tr> 
</table>

Utilisé pour contrôler l’effet de rendu de la réflexion 3D. Les valeurs de rugosité inférieure produisent généralement des effets de réflexion plus fluides; des valeurs plus élevées entraînent l’organisation aléatoire et la dispersion de l’image reflétée.

Chaque type de matériau ( `type=`) définit un effet de rendu de réflexion minimal et maximal basé sur la rugosité. Pour certains types de matériaux (comme le papier peint), `rough=` n&#39;a guère d&#39;impact sur l&#39;aspect de la réflexion, alors que pour d&#39;autres types de matériaux (comme la pierre ou la céramique), l&#39;effet est sensiblement plus prononcé.

`rough=-1` définit la rugosité sur une valeur par défaut interne au serveur (40 % pour les types de matériaux standard).

## Propriétés {#section-515375758b254c80af576271bdb61bb8}

Attribut de matière. Ignoré si la vignette n’a pas de fonction de réflexion 3D, si la géométrie de l’objet cible n’est pas associée à l’objet cible ou si l’objet cible ne reflète aucun autre objet de la scène.

## Par défaut {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` si le matériau est basé sur une entrée de catalogue, sinon environ 40 %.

## Voir aussi {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ,  [gless=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
