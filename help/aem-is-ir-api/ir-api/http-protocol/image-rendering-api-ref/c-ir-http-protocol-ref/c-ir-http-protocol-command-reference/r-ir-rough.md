---
description: La rugosité de la surface du matériau. Indique la rugosité relative de la surface du matériau.
solution: Experience Manager
title: brut
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# rugueux{#rough}

La rugosité de la surface du matériau. Indique la rugosité relative de la surface du matériau.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Rogosité de surface (0...100 %) ou -1 pour sélectionner la rugosité par défaut. </p> </td> 
 </tr> 
</table>

Utilisé pour contrôler l’effet de rendu de la réflexion 3D. Les valeurs de rugosité inférieures produisent généralement des effets de réflexion plus lisses ; des valeurs plus élevées provoquent l’organisation aléatoire et la dispersion de l’image réfléchie.

Chaque type de matériau ( `type=`) définit un effet de rendu de réflexion minimum et maximum basé sur la rugosité. Pour certains types de matériaux (p. ex. papier peint), `rough=` n&#39;a guère d&#39;impact sur l&#39;aspect de la réflexion, alors que pour d&#39;autres types de matériaux (p. ex. pierre ou céramique), l&#39;effet est beaucoup plus prononcé.

`rough=-1` définit la rugosité sur une valeur par défaut interne au serveur (40 % pour les types de matériaux standard).

## Propriétés {#section-515375758b254c80af576271bdb61bb8}

Attribut de matériau. Ignoré si la vignette n&#39;a pas de fonction de réflexion 3D, si l&#39;objet cible n&#39;est associé à aucune géométrie 3D ou si l&#39;objet cible ne reflète aucun autre objet de la scène.

## Par défaut {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` si le matériel est basé sur une entrée de catalogue, sinon environ 40 %.

## Voir aussi {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ,  [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
