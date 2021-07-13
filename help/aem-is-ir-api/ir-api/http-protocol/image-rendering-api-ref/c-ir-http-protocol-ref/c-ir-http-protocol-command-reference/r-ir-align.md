---
description: Alignement du rendu de la texture. Indique les points d’origine définis par l’objet de vignette sélectionné à utiliser.
solution: Experience Manager
title: align
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---

# align{#align}

Alignement du rendu de la texture. Indique les points d’origine définis par l’objet de vignette sélectionné à utiliser.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p></td> 
  <td class="stentry"> <p>Origine par défaut (correspondance centrale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Origine continue de la correspondance. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alignement aléatoire. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>Origine définie par l’utilisateur. </p></td> 
 </tr> 
</table>

Le moteur de rendu applique la texture à l’objet de sorte que le point d’ancrage de la texture ( `anchor=`) coïncide avec le point d’origine spécifié.

Chaque objet peut définir jusqu’à 6 points d’origine (0,1, 3, 4, 5, 6). Si une valeur `align` est spécifiée mais que le point d’origine correspondant n’est pas défini par l’objet de vignette, le point d’origine par défaut (centrmatch) est utilisé.

`align=2` spécifie un alignement de texture aléatoire, auquel cas  `anchor=` est effectivement ignoré.

Utilisé principalement pour les matériaux de toile, éventuellement pour les tissus d&#39;habillement, afin de gérer l&#39;alignement de la texture entre les objets adjacents.

## Propriétés {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Attribut de matière. Ignoré si un objet cadre de paroi, d’armoire, d’appareil ou de fenêtre est sélectionné ou si la matière n’est pas une texture répétable.

## Par défaut {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, si le contenu est basé sur une entrée de catalogue, sinon 0 (correspondant au centre).

## Voir aussi {#section-945d1ce275df487d9d564d4043156c79}

[catalogue : Alignement](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
