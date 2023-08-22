---
title: rect
description: Rectangle de la vue finale. Permet le démontage de l’image d’affichage final en plusieurs bandes ou mosaïques, qui peuvent être diffusées séparément et reassemblées par le client de manière transparente, sans artefacts le long des bords.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 1%

---

# rect{#rect}

Rectangle de la vue finale. Permet le démontage de l’image d’affichage final en plusieurs bandes ou mosaïques, qui peuvent être diffusées séparément et reassemblées par le client de manière transparente, sans artefacts le long des bords.

`rect= *`coord`*, *`size`*[, *`scale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Décalage des pixels du coin supérieur gauche de l’image de la vue vers le coin supérieur gauche du rectangle de la vue (int, int), exprimé en pixels, après <span class="varname"> scale</span> est appliquée. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> taille</span> </p></td> 
  <td class="stentry"> <p>Taille du ROI en pixels (int, int). Indique la taille de l’image de réponse. L’image est remplie de <span class="codeph"> bgc=</span> dans les zones non couvertes par l’image d’affichage (ou laissées transparentes, si <span class="codeph"> fmt=*-alpha</span> est présent dans la requête). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Facteur d’échelle (réel). Les valeurs inférieures à 1,0 réduisent la résolution et les valeurs supérieures à 1,0 augmentent la résolution. </p></td> 
 </tr> 
</table>

Avec cette commande, la diffusion d’images peut diffuser des images de grande taille via HTTP qui, sinon, dépasseraient la taille limite configurée avec `attribute::MaxPix`.

>[!NOTE]
>
>Pour de meilleurs résultats lorsque la compression JPEG est utilisée, la taille de la bande ou de la mosaïque doit correspondre à un multiple de la taille de la mosaïque de codage du JPEG (16x16 pixels).

## Exemple {#section-932fcfcb41d74a29bc929e4430c49601}

Séparez une image CMJN imprimable en plusieurs bandes pleine résolution afin de réduire la taille des fichiers de téléchargement. Si nous devions demander une image contiguë :

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Tout d’abord, vous obtenez des informations pertinentes sur l’image :

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

La réponse textuelle comprend les propriétés suivantes :

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Sur la base de ces informations, nous décidons que nous voulons quatre bandes de 600x2000 pixels. La variable `rect=` sert à décrire les tailles et les positions des bandes.

Comme cette image est fréquemment modifiée, nous inclurons la variable `id=` afin de minimiser les risques que nous ayons une ou plusieurs bandes d’une ancienne version de l’image qui ont pu être mises en cache dans un réseau de diffusion de contenu ou un serveur proxy. La valeur de la variable `image.version` est utilisée à cette fin.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Propriétés {#section-aae223cee13e46d38b74680c048d945b}

Attribut d’affichage. S’applique quel que soit le paramètre de calque actif.

Toutes les zones du ROI situées en dehors de l’image d’affichage sont remplies par `bgc=`.

Important `rect=` est appliqué *after* mise à l’échelle finale et ajustement avec `scl=`, `wid=`, `hei=`, `fit=`, `rgn=`, et `align=`.

## Par défaut {#section-b296d3bbfb19441f87137a452b70f19a}

Image de vue entière non modifiée ( `rect=0,0,width,height,1.0`).

## Voir également {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
