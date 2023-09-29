---
title: Taille
description: Taille des décimales. Largeur, hauteur et épaisseur d’un objet de matériau décal.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 4%

---

# Taille{#size}

Taille des décimales. Largeur, hauteur et épaisseur d’un objet de matériau décal.

## Propriétés {#section-967bf1112eec4032a91ed0c8a7b10a07}

Trois nombres réels séparés par des virgules. Elle ne doit pas être négative. Définissez les valeurs inutilisées sur 0. Des zéros de fin peuvent être omis.

Spécifiez la largeur et la hauteur uniquement si l’image doit être étirée pour l’adapter à la taille spécifiée (le rapport d’aspect peut changer). Définissez la largeur ou la hauteur pour mettre l’image à l’échelle proportionnellement. Définissez la largeur et la hauteur sur 0 pour utiliser `catalog::Resolution`pour déterminer la taille de l’objet.

Fournissez une valeur d’épaisseur pour ajouter une ombre portée à l’objet de décal. Facultatif pour les matériaux décals, ignorés par tous les autres matériaux.

## Par défaut {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Cela indique que la taille des décimales doit être déterminée en fonction de catalog::Resolution et que l’objet n’a pas d’épaisseur (aucune ombre portée n’est donc générée).

## Exemples {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>La décimale est forcée à 12x3 pouces de taille et n’a pas d’épaisseur (c’est-à-dire, pas d’ombre portée). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>La décimale fait 5 pouces de large, la hauteur est déterminée par le rapport d’aspect de l’image et une ombre portée est générée selon une épaisseur de 1 pouce. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>La largeur et la hauteur des décimales sont déterminées par le catalogue ::résolution, et qu’elles sont d’une épaisseur d’un demi-pouce. </p></td> 
 </tr> 
</table>

## Voir aussi {#section-31a164e781d14e92bd9d379d3c329e92}

[catalogue : résolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
