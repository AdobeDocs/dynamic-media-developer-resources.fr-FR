---
title: aligner
description: Alignement du rendu de la texture. Spécifie le point d'origine défini par l'objet vignette sélectionné à utiliser.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 3%

---

# aligner {#align}

Alignement du rendu de la texture. Spécifie le point d&#39;origine défini par l&#39;objet vignette sélectionné à utiliser.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p></td> 
  <td class="stentry"> <p>Origine par défaut (correspondance centrale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Origine de correspondance continue. </p></td> 
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

Le rendu applique la texture à l’objet de sorte que le point d’ancrage de texture ( `anchor=`) corresponde au point d’origine spécifié.

Chaque objet peut définir jusqu’à six points d’origine (0, 1, 3, 4, 5, 6). Si une valeur `align` est spécifiée mais que le point d’origine correspondant n’est pas défini par l’objet vignette, le point d’origine par défaut (correspondance centrale) est utilisé.

`align=2` Spécifie l&#39;alignement aléatoire des textures, auquel cas `anchor=` est effectivement ignoré.

Principalement utilisé pour les matériaux d&#39;ameublement, éventuellement pour les tissus d&#39;habillement, pour gérer l&#39;alignement de la texture entre les objets adjacents.

## Propriétés {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Attribut Material. Ignoré si un objet de cadre de mur, d&#39;armoire, d&#39;appareil ou de revêtement de fenêtre est sélectionné ou si la matière n&#39;est pas une texture répétable.

## Par défaut {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, si le matériau est basé sur une entrée de catalogue, sinon 0 (centré).

## Voir aussi {#section-945d1ce275df487d9d564d4043156c79}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
