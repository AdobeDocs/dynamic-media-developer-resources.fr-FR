---
description: Taille Jpeg en kiloBytes. Indique la taille maximale de la réponse JPEG en kilo-octets.
solution: Experience Manager
title: jpegSize
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 4%

---


# jpegSize{#jpegsize}

Taille Jpeg en kiloBytes. Indique la taille maximale de la réponse JPEG en kilo-octets.

`jpegSize= *`taille`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> taille</span></span> </p> </td> 
  <td class="stentry"> <p>Taille en kilo-octets. </p></td> 
 </tr> 
</table>

Si cette valeur est définie sur une valeur positive et si la réponse JPEG avec la qualité JPEG spécifiée ne dépasse pas cette valeur, cette image est renvoyée comme réponse. Sinon, la qualité JPEG diminue jusqu’à ce qu’elle produise une image qui correspond à la taille spécifiée ou jusqu’à ce qu’elle détermine qu’elle ne peut pas tenir. Dans ce dernier cas, la requête échoue avec une erreur.

La valeur 0 signifie que la réponse n’est pas limitée par la taille.

Les valeurs négatives ne sont pas autorisées.

## Propriétés {#section-19e544e77d35478b98fe8666f27d6968}

Attribut de requête. S’applique quel que soit le paramètre de calque actif. Ignoré si le format d’image de sortie n’est pas JPEG.

## Par défaut {#section-198b798ed187453197e0969c641d6fb5}

01

## Exemple {#section-46bf806fd3ef4875b7726df32b6f834d}

La taille de la garantie n&#39;est pas trop grande pour être livrée à un périphérique avec une mémoire limitée :

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Voir aussi {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [attribut::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
