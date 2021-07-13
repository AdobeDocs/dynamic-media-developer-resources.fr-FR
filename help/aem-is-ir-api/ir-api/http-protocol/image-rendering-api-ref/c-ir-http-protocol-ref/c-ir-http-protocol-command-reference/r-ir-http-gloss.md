---
description: Matériau de brillance de surface. Indique la brillance relative de la surface du matériau. Utilisé pour sélectionner la carte d'éclairage et contrôler le rendu des effets de brillance et des reflets 3D.
solution: Experience Manager
title: gèle
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---

# gèle{#gloss}

Matériau de brillance de surface. Indique la brillance relative de la surface du matériau. Utilisé pour sélectionner la carte d&#39;éclairage et contrôler le rendu des effets de brillance et des reflets 3D.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Glessure (0...100 %) ou -1 pour la valeur d’éclat par défaut (référence). </p></td> 
 </tr> 
</table>

Des valeurs de brillance plus élevées provoquent généralement des reflets plus forts et plus nets, et si des effets de brillance sont activés dans la vignette, cela renforce les reflets spéculaires sur la surface du matériau, principalement en augmentant le contraste d’éclairage. Chaque type de matériau ( `type=`) définit un effet de rendu minimal et maximal. Pour certains types de matériaux (p. ex. le papier peint), `gloss=` n&#39;a guère d&#39;impact sur l&#39;aspect de l&#39;effet de rendu, alors que pour d&#39;autres types de matériaux (p. ex. la pierre ou la céramique), l&#39;effet est sensiblement plus prononcé.

Si `illum=-1` et que la vignette définit plusieurs cartes d’éclairage, `gloss=` sélectionne la carte d’éclairage utilisée pour l’opération de rendu actuelle. Le moteur de rendu choisit la carte d’éclairage dont la valeur de brillance est la plus proche de la brillance spécifiée.

`gloss=-1` sélectionne la valeur d’éclat de référence de la carte d’éclairage sélectionnée, telle que définie dans les propriétés d’affichage de la vignette. Cela permet de s’assurer que la carte d’éclairage est utilisée exactement comme créée, sans modification supplémentaire, même si les effets d’éclat sont activés. Si `illum=-1` est également utilisé, la valeur d’éclair de référence de la première carte d’éclairage dans la vue de vignette.

## Propriétés {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Attribut de matière. Ignoré si la vignette ne définit pas plusieurs cartes d’éclairage ou si `illum=` est spécifié, si la vignette n’inclut pas de données de réflexion 3D ou si l’objet actif ne prend pas en charge les reflets 3D, ou si les effets d’éclat sont désactivés dans la vignette.

## Par défaut {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` si le matériau est basé sur une entrée de catalogue, sinon la valeur de brillance de référence de la carte d’éclairage par défaut ou de la carte d’éclairage spécifiée par  `illum=`.

## Voir aussi {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Glessure](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35),  [rugueux=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180),  [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a),  [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
