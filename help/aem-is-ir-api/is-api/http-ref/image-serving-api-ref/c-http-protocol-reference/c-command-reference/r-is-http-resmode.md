---
title: resMode
description: Mode de rééchantillonnage. Choisit l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour mettre à l’échelle les données d’image. S’applique également à la rotation des calques de texte et au redimensionnement des images composites lors de la transformation de la vue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
TQID: 'https://experienceleague.adobe.com/uT9SBMqQ0JvU-S8BF2y0kY6C--jNhvggbRwhTpTJOGg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 1%

---

# resMode{#resmode}

Mode de rééchantillonnage. Choisit l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour mettre à l’échelle les données d’image. S’applique également à la rotation des calques de texte et au redimensionnement des images composites lors de la transformation de la vue.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne l’interpolation bilinéaire standard. Méthode de rééchantillonnage la plus rapide ; certains artefacts d’alias sont visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> bicub </p> </td> 
   <td colname="col2"> <p>Sélectionne l'interpolation bi-cubique. Plus gourmande en CPU qu’une interpolation bilinéaire, mais offre des images plus nettes avec des artefacts de crénelage moins visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne une fonction Lanczos Window modifiée comme algorithme d'interpolation. Peut produire des résultats légèrement plus nets que bi-cubique à un coût CPU plus élevé. <span class="codeph"> flou </span> a été remplacé par <span class="codeph"> flou2 </span>, qui a moins de chances de causer des artefacts d'alias (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne le rééchantillonnage par défaut de Photoshop pour réduire la taille de l’image, qui est appelé « accentuateur bicubique » dans Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Pour conserver les proportions d’une image lorsque vous utilisez à la fois `resMode=bisharp` et `fit=stretch`, il est recommandé d’utiliser le paramètre de largeur ou de hauteur. Si les deux paramètres doivent être définis, vous pouvez les encapsuler dans un calque différent, comme illustré dans l’exemple suivant :
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Propriétés {#section-a171bacf4ddf43c782e46b86a16d443e}

Attribut de requête. S’applique à toutes les opérations de mise à l’échelle impliquées dans la création de l’image de réponse finale, y compris la mise à l’échelle des calques.

## Par défaut {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Exemple {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Récupérez un rendu de meilleure qualité d’une image superposée stockée dans un catalogue d’images. L’image peut inclure du texte. L&#39;image est ensuite traitée dans une application d&#39;édition d&#39;image, et demande ainsi un canal alpha avec l&#39;image.

` http:// *`serveur`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Voir aussi {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
