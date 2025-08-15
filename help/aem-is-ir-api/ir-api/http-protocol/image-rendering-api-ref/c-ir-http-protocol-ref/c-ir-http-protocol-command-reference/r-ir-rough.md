---
title: rude
description: Rugosité de surface du matériau. Indique la rugosité relative de la surface du matériau.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# rude{#rough}

Rugosité de surface du matériau. Indique la rugosité relative de la surface du matériau.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Rugosité de surface (0...100 %) ou -1 pour sélectionner la rugosité par défaut. </p> </td> 
 </tr> 
</table>

Permet de contrôler l’effet de rendu de réflexion 3D. Des valeurs de rugosité plus faibles produisent généralement des effets de réflexion plus lisses ; des valeurs plus élevées entraînent une randomisation et une diffusion de l&#39;image réfléchie.

Chaque type de matériau (`type=`) définit un effet de rendu de réflexion minimum et maximum en fonction de la rugosité. Pour certains types de matériaux (par exemple, le papier peint), `rough=` a un impact minimal sur l&#39;aspect du reflet, tandis que pour d&#39;autres types de matériaux (par exemple, la pierre ou la céramique), l&#39;effet est sensiblement plus prononcé.

`rough=-1` Définit la rugosité sur une valeur par défaut interne au serveur (40 % pour les types de matériaux standard).

## Propriétés {#section-515375758b254c80af576271bdb61bb8}

Attribut Material. Ignoré si la vignette ne possède aucune capacité de réflexion 3D, si l&#39;objet cible n&#39;est pas associé à une géométrie 3D ou si l&#39;objet cible ne reflète aucun autre objet de la scène.

## Par défaut {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` Si le matériel est basé sur une entrée de catalogue, sinon environ 40 %.

## Voir aussi {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
