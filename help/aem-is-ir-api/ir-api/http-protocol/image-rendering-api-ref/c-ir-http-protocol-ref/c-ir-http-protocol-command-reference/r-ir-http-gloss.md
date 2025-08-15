---
title: briller
description: Brillance de la surface du matériau. Indique la brillance relative de la surface du matériau. Permet de sélectionner la carte d'illumination et de contrôler le rendu des effets de brillance et des réflexions 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# briller{#gloss}

Brillance de la surface du matériau. Indique la brillance relative de la surface du matériau. Permet de sélectionner la carte d&#39;illumination et de contrôler le rendu des effets de brillance et des réflexions 3D.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Brillance (0...100 %) ou -1 pour la valeur de brillance par défaut (de référence). </p></td> 
 </tr> 
</table>

Des valeurs de brillance plus élevées entraînent généralement des réflexions plus fortes et plus nettes et, si les effets de brillance sont activés dans la vignette, renforcent les reflets spéculaires sur la surface du matériau, principalement en augmentant le contraste d&#39;éclairage. Chaque type de matériau (`type=`) définit un effet de rendu minimum et maximum. Pour certains types de matériaux (par exemple, le papier peint), `gloss=` a un impact minimal sur l’apparence de l’effet de rendu, tandis que pour d’autres types de matériaux (par exemple, la pierre ou la céramique), l’effet est nettement plus prononcé.

Si `illum=-1` et si la vignette définit plusieurs textures d&#39;illumination, `gloss=` sélectionne la texture d&#39;illumination utilisée pour l&#39;opération de rendu actuelle. Le moteur de rendu choisit la texture d&#39;illumination dont la valeur de brillance est la plus proche de la brillance spécifiée.

`gloss=-1` Sélectionne la valeur de brillance de référence de la texture d&#39;éclairage sélectionnée, telle que définie dans les propriétés d&#39;affichage de la vignette. Cette valeur garantit que la texture d&#39;éclairage est utilisée exactement comme elle a été créée, sans autre modification, même si les effets de brillance sont activés. Si `illum=-1`, la valeur de brillance de référence de la première carte d&#39;illumination en vue vignette est utilisée.

## Propriétés {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Attribut Material. Ignoré si la vignette ne définit pas plusieurs cartes d&#39;illumination. Ou, si `illum=` est spécifié, si la vignette n&#39;inclut pas de données de réflexion 3D. Ou si l&#39;objet courant ne prend pas en charge les réflexions 3D ou si les effets de brillance sont désactivés dans la vignette.

## Par défaut {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` Si le matériau est basé sur une entrée de catalogue, sinon la valeur de brillance de référence de la texture d&#39;éclairage par défaut ou de la texture d&#39;éclairage spécifiée par `illum=`.

## Voir aussi {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [raw=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
