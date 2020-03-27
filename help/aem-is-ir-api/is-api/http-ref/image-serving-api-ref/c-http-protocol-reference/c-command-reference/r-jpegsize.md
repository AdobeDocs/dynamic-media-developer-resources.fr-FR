---
description: Taille Jpeg en Ko. Indique la taille maximale de la réponse JPEG en kilo-octets.
seo-description: Taille Jpeg en Ko. Indique la taille maximale de la réponse JPEG en kilo-octets.
seo-title: jpegSize
solution: Experience Manager
title: jpegSize
topic: Scene7 Image Serving - Image Rendering API
uuid: 832163ca-0554-481d-b87f-bf322f415274
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# jpegSize{#jpegsize}

Taille Jpeg en Ko. Indique la taille maximale de la réponse JPEG en kilo-octets.

`jpegSize= *`taille`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> taille</span></span> </p> </td> 
  <td class="stentry"> <p>Taille en kilo-octets. </p></td> 
 </tr> 
</table>

Si cette valeur est définie sur une valeur positive et si la réponse JPEG avec la qualité JPEG spécifiée ne dépasse pas cette valeur, cette image est renvoyée comme réponse. Dans le cas contraire, la qualité JPEG diminue jusqu’à ce qu’elle produise une image qui s’adapte à la taille spécifiée ou jusqu’à ce qu’elle détermine qu’elle ne s’adapte pas. Dans ce dernier cas, la requête échoue avec une erreur.

La valeur 0 signifie que la réponse n’est pas restreinte par la taille.

Les valeurs négatives ne sont pas autorisées.

## Propriétés {#section-19e544e77d35478b98fe8666f27d6968}

Attribut de requête. S’applique indépendamment du paramètre de calque actif. Ignoré si le format d’image de sortie n’est pas JPEG.

## Par défaut {#section-198b798ed187453197e0969c641d6fb5}

01

## Exemple {#section-46bf806fd3ef4875b7726df32b6f834d}

La taille de la garantie n&#39;est pas trop grande pour être livrée à un périphérique avec une mémoire limitée :

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Voir aussi {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribut::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
