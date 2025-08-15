---
title: Taille
description: Taille de décalcomanie. Largeur, hauteur et épaisseur d’un objet de matériau de décalcomanie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 3%

---

# Taille{#size}

Taille de décalcomanie. Largeur, hauteur et épaisseur d’un objet de matériau de décalcomanie.

## Propriétés {#section-967bf1112eec4032a91ed0c8a7b10a07}

Trois nombres réels séparés par des virgules. Elle ne doit pas être négative. Définissez les valeurs inutilisées sur 0. Les zéros à droite peuvent être omis.

Spécifiez à la fois la largeur et la hauteur uniquement si l’image doit être étirée pour correspondre à la taille spécifiée (le rapport hauteur/largeur peut changer). Définissez la largeur ou la hauteur pour mettre l’image à l’échelle proportionnellement. Définissez la largeur et la hauteur sur 0 afin de déterminer la taille de l’objet `catalog::Resolution`.

Fournissez une valeur d’épaisseur pour ajouter une ombre portée à l’objet décalcomanie. Facultatif pour les matériaux de décalcomanie, ignoré par tous les autres matériaux.

## Par défaut {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Cela indique que la taille des décalcomanies doit être déterminée en fonction de catalog ::Resolution, et que l’objet n’a pas d’épaisseur (par conséquent, aucune ombre portée n’est rendue).

## Exemples {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>L’autocollant est forcé à 12x3 pouces de taille et n’a pas d’épaisseur (c’est-à-dire pas d’ombre portée). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>L’autocollant mesure 5 pouces de large, la hauteur est déterminée par le format de l’image et une ombre portée est rendue en fonction d’une épaisseur de 1 pouce. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>La largeur et la hauteur de l’autocollant sont déterminées par catalog ::Resolution, et qu’il est de 1/2 pouce d’épaisseur. </p></td> 
 </tr> 
</table>

## Voir aussi {#section-31a164e781d14e92bd9d379d3c329e92}

[catalogue ::Résolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
