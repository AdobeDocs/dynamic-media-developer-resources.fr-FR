---
description: Alignement du rendu de la texture. Indique les points  du  définis par l’objet de vignette sélectionné à utiliser.
seo-description: Alignement du rendu de la texture. Indique les points  du  définis par l’objet de vignette sélectionné à utiliser.
seo-title: aligner
solution: Experience Manager
title: aligner
topic: Scene7 Image Serving - Image Rendering API
uuid: 0b24cd82-f9b2-48f4-9052-8c2026370ff7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# align{#align}

Alignement du rendu de la texture. Indique les points  du  définis par l’objet de vignette sélectionné à utiliser.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p></td> 
  <td class="stentry"> <p> par défaut (centre-correspondance) . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Correspondance continue  . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alignement aléatoire. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p> défini par l’utilisateur . </p></td> 
 </tr> 
</table>

Le rendu applique la texture à l’objet de sorte que le point d’ancrage de la texture ( `anchor=`) coïncide avec le point   spécifié.

Chaque objet peut définir jusqu’à 6 points   (0,1, 3, 4, 5, 6). Si une `align` valeur est spécifiée, mais que le point  du correspondant n’est pas défini par l’objet de vignette, le point de  par défaut (correspondance centrale) est utilisé.

`align=2` spécifie un alignement de texture aléatoire, auquel cas `anchor=` est effectivement ignoré.

Utilisé principalement pour les matériaux de rembourrage, éventuellement pour les tissus de vêtements, pour gérer l’alignement de la texture entre les objets adjacents.

## Propriétés {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Attribut de matière. Ignoré si un objet cadre de recouvrement de mur, d’armoire, d’appliance ou de fenêtre est sélectionné ou si le matériau n’est pas une texture répétable.

## Par défaut {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, si le matériau est basé sur une entrée de catalogue, sinon 0 (correspondance centrale).

## Voir aussi {#section-945d1ce275df487d9d564d4043156c79}

[catalogue ::Alignement](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [ancrage=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
