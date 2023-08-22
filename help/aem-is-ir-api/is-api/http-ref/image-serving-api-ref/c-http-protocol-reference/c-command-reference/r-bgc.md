---
title: bgc
description: Afficher la couleur de fond. Indique la couleur d’arrière-plan de l’image composite (vue image).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# bgc{#bgc}

Afficher la couleur de fond. Indique la couleur d’arrière-plan de l’image composite (vue image).

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span></span> </p> </td> 
  <td class="stentry"> <p>Valeur de couleur grise, RGB ou CMJN. </p></td> 
 </tr> 
</table>

Spécifie une couleur de fond opaque à utiliser pour l’arrière-plan de la vue. Visible uniquement si l’image composite comporte des zones transparentes ou si l’image composite a des proportions différentes du rectangle de l’affichage. Ignoré si `fmt=tif-alpha` ou `fmt=png-alpha`, ou `req=mask`.

>[!NOTE]
>
>Le suffixe de couleur &quot;s&quot; est ignoré par `bgc=`. Valeurs de couleur spécifiées avec `bgc=` sont toujours associés à l’espace colorimétrique de sortie correspondant.

## Propriétés {#section-b729b50b1ea7433b82ba34ecd61839cd}

Attribut d’affichage. S’applique quel que soit le paramètre de calque actif. Ignoré si `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha`, ou `fmt=swf-alpha`.

Toute valeur alpha spécifiée avec la couleur est ignorée.

*`color`* est supposé appartenir à l’espace colorimétrique de sortie (comme spécifié avec `icc=`) et doit avoir le même type de pixel que l’image de sortie. Si les types de pixels ne correspondent pas, *`color`* est converti à l’aide d’une conversion naïve.

## Par défaut {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Exemple {#section-7bcdfbc0e1274e86a69d39186b090789}

Spécifiez une couleur d’arrière-plan explicite pour une demande de miniature :

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## Voir aussi {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Gestion des couleurs](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
