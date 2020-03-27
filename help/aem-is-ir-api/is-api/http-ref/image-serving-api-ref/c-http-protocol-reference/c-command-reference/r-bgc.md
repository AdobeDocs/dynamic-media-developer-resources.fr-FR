---
description: Couleur d’arrière-plan . Indique la couleur d’arrière-plan de l’image composite (image ).
seo-description: Couleur d’arrière-plan . Indique la couleur d’arrière-plan de l’image composite (image ).
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 3ea8291e-3223-45ff-a2ad-43fc212eff90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgc{#bgc}

Couleur d’arrière-plan . Indique la couleur d’arrière-plan de l’image composite (image ).

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> couleur</span></span> </p> </td> 
  <td class="stentry"> <p>Valeur de couleur Gris, RVB ou CMJN. </p></td> 
 </tr> 
</table>

Indique une couleur de remplissage opaque à utiliser pour l’arrière-plan  du. Visible uniquement si l’image composite comporte des zones transparentes ou si les proportions de l’image composite sont différentes de celles du rectangle . Ignoré si `fmt=tif-alpha` ou `fmt=png-alpha`, ou `req=mask`.

>[!NOTE]
>
>Le suffixe de couleur &quot;s&quot; est ignoré par `bgc=`. Les valeurs de couleur spécifiées avec `bgc=` sont toujours associées à l’espace colorimétrique de sortie correspondant.

## Propriétés {#section-b729b50b1ea7433b82ba34ecd61839cd}

attribut . S’applique indépendamment du paramètre de calque actif. Ignoré si `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha`ou `fmt=swf-alpha`.

Toute valeur alpha spécifiée avec la couleur est ignorée.

*`color`* est supposée appartenir à l’espace colorimétrique de sortie (comme indiqué dans `icc=`) et doit avoir le même type de pixel que l’image de sortie. Si les types de pixels ne correspondent pas, *`color`* est converti à l’aide d’une conversion naïve.

## Par défaut {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Exemple {#section-7bcdfbc0e1274e86a69d39186b090789}

Spécifiez une couleur d’arrière-plan explicite pour une demande de miniature :

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## Voir aussi {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribut::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), icc=, Gestion des couleurs de lasuite[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
