---
title: Taille
description: Taille de la vignette. Largeur, hauteur et épaisseur d’un objet en matériau de vignette.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
TQID: 'https://experienceleague.adobe.com/HLyEmmOch9kiHQ3sqpvHCQiHOBltjQcsZaDu0na1-Ww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 217
ht-degree: 5%

---

# Taille{#size}

Taille de la vignette. Largeur, hauteur et épaisseur d’un objet en matériau de vignette.

## Propriétés {#section-967bf1112eec4032a91ed0c8a7b10a07}

Trois nombres réels séparés par des virgules. Il ne doit pas être négatif. Définissez les valeurs inutilisées sur 0. Les zéros de fin peuvent être omis.

Indiquez la largeur et la hauteur uniquement si l’image doit être étirée pour s’adapter à la taille spécifiée (les proportions peuvent changer). Définissez la largeur ou la hauteur pour mettre l’image à l’échelle proportionnellement. Définissez la largeur et la hauteur sur 0 pour utiliser `catalog::Resolution`pour déterminer la taille de l’objet.

Fournissez une valeur d&#39;épaisseur pour ajouter une ombre portée à l&#39;objet décalque. Facultatif pour les matières de vignette, ignoré par toutes les autres matières.

## Par défaut {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Cela indique que la taille de la vignette doit être déterminée en fonction de catalog::Resolution et que l&#39;objet n&#39;a pas d&#39;épaisseur (par conséquent, aucune ombre portée n&#39;est rendue).

## Exemples {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>La vignette est forcée à une taille de 12 x 3 pouces et n'a pas d'épaisseur (c'est-à-dire, pas d'ombre portée). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>La vignette a une largeur de 5 pouces, la hauteur est déterminée par le format de l’image et une ombre portée est rendue sur une épaisseur de 1 pouce. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>La largeur et la hauteur de la vignette sont déterminées par catalog::Resolution, et elle a une épaisseur de ½ pouce. </p></td> 
 </tr> 
</table>

## Voir aussi {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)

