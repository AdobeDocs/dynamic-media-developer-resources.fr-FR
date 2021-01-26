---
description: Mode de rééchantillonnage. Choisit l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour la mise à l’échelle des données d’image. S’applique également à la rotation des calques de texte et au redimensionnement des images composites pendant la transformation de la vue.
seo-description: Mode de rééchantillonnage. Choisit l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour la mise à l’échelle des données d’image. S’applique également à la rotation des calques de texte et au redimensionnement des images composites pendant la transformation de la vue.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 12%

---


# resMode{#resmode}

Mode de rééchantillonnage. Choisit l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour la mise à l’échelle des données d’image. S’applique également à la rotation des calques de texte et au redimensionnement des images composites pendant la transformation de la vue.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> biline  </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne l’interpolation bilinéaire standard. Il s’agit de la méthode de ré-échantillonnage la plus rapide ; certains artefacts de crénelage peuvent être visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne l’interpolation bicubique. Plus intensif en UC que l’interpolation bi-linéaire, mais produira des images plus nettes avec des artefacts de crénelage moins visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne une fonction Lanczos Window modifiée comme algorithme d'interpolation. Peut produire des images légèrement plus nettes que la méthode bicubique en sollicitant toutefois davantage le processeur. <span class="codeph"> sharp  </span> a été remplacé par  <span class="codeph"> sharp2  </span>, qui a une probabilité moindre de causer des artefacts de crénelage (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> évêque  </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne le rééchantillonneur par défaut Photoshop pour réduire la taille de l’image, appelée "netteté bicubique" dans Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-a171bacf4ddf43c782e46b86a16d443e}

Attribut de requête. S’applique à toutes les opérations de mise à l’échelle impliquées dans la création de l’image de réponse finale, y compris la mise à l’échelle de tous les calques.

## Par défaut {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Exemple {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Récupérez un rendu de meilleure qualité d’une image superposée stockée dans un catalogue d’images. L’image peut inclure du texte. Nous prévoyons de continuer le traitement dans une application de retouche d&#39;images, et donc de demander un canal alpha avec l&#39;image.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Voir aussi {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribut::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
