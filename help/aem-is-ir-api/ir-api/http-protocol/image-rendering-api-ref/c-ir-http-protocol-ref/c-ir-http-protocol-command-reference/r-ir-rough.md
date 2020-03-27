---
description: La rugosité de surface du matériau. Indique la rugosité relative de la surface du matériau.
seo-description: La rugosité de surface du matériau. Indique la rugosité relative de la surface du matériau.
seo-title: rugueux
solution: Experience Manager
title: rugueux
topic: Scene7 Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rugueux{#rough}

La rugosité de surface du matériau. Indique la rugosité relative de la surface du matériau.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Rogosité de surface (0...100 %) ou -1 pour sélectionner la rugosité par défaut. </p> </td> 
 </tr> 
</table>

Permet de contrôler l’effet de rendu du reflet 3D. Les valeurs de rugosité inférieure produisent généralement des effets de réflexion plus fluides; des valeurs plus élevées provoquent la randomisation et la dispersion de l’image réfléchie.

Chaque type de matériau ( `type=`) définit un effet de rendu de réflexion minimal et maximal basé sur la rugosité. Pour certains types de matériaux (p. ex., le papier peint), `rough=` n&#39;a guère d&#39;impact sur l&#39;apparence de la réflexion, alors que pour d&#39;autres types de matériaux (p. ex., la pierre ou la céramique), l&#39;effet est beaucoup plus prononcé.

`rough=-1` définit la rugosité sur une valeur par défaut interne au serveur (40 % pour les types de matériaux standard).

## Propriétés {#section-515375758b254c80af576271bdb61bb8}

Attribut de matière. Ignoré si la vignette n’a pas de fonction de réflexion 3D, si l’objet  n’est associé à aucune géométrie 3D ou si l’objet  ne reflète aucun autre objet de la scène.

## Par défaut {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` si le matériau est basé sur une entrée de catalogue, sinon environ 40 %.

## Voir aussi {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
