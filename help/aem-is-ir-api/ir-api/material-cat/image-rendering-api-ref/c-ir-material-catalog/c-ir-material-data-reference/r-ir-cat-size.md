---
description: Taille de la poule. Largeur, hauteur et épaisseur d’un objet de matériau de décomposition.
seo-description: Taille de la poule. Largeur, hauteur et épaisseur d’un objet de matériau de décomposition.
seo-title: Taille
solution: Experience Manager
title: Taille
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 5%

---


# Taille{#size}

Taille de la poule. Largeur, hauteur et épaisseur d’un objet de matériau de décomposition.

## Propriétés {#section-967bf1112eec4032a91ed0c8a7b10a07}

Trois nombres réels séparés par des virgules. Ne doit pas être négatif. Définissez les valeurs inutilisées sur 0. Des zéros de fin peuvent être omis.

Spécifiez à la fois la largeur et la hauteur uniquement si l’image doit être étirée pour correspondre à la taille spécifiée (les proportions peuvent changer). Définissez la largeur ou la hauteur pour mettre l’image à l’échelle proportionnellement. Définissez la largeur et la hauteur sur 0 pour utiliser `catalog::Resolution`afin de déterminer la taille de l’objet.

Fournissez une valeur d’épaisseur pour ajouter une ombre portée à l’objet decal. Facultatif pour les matériaux à décale, ignorés par tous les autres matériaux.

## Par défaut {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Cela indique que la taille de la poubelle doit être déterminée en fonction de catalog::Resolution et que l’objet n’a pas d’épaisseur (aucune ombre portée ne sera donc générée).

## Exemples {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>La poule est forcée à 12x3 pouces de taille et n'a pas d'épaisseur (c'est-à-dire pas d'ombre portée). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>La vignette fait 5 pouces de large, la hauteur est déterminée par le format de l’image et une ombre portée est générée en fonction d’une épaisseur de 1 pouce. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,,5 </p></td> 
  <td class="stentry"> <p>La largeur et la hauteur des décalcomanies sont déterminées par catalog::Resolution et sont d'une épaisseur d'un demi-pouce. </p></td> 
 </tr> 
</table>

## Voir aussi {#section-31a164e781d14e92bd9d379d3c329e92}

[catalogue : résolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
