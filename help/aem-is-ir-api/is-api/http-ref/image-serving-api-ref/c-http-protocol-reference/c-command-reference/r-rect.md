---
description: Rectangle  final du. Permet de démonter l’image finale du en plusieurs bandes ou mosaïques, qui peuvent être livrées séparément et reassemblées par le client en toute simplicité, sans artefacts le long des bords.
seo-description: Rectangle  final du. Permet de démonter l’image finale du en plusieurs bandes ou mosaïques, qui peuvent être livrées séparément et reassemblées par le client en toute simplicité, sans artefacts le long des bords.
seo-title: rect
solution: Experience Manager
title: rect
topic: Scene7 Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rect{#rect}

Rectangle  final du. Permet de démonter l’image finale du en plusieurs bandes ou mosaïques, qui peuvent être livrées séparément et reassemblées par le client en toute simplicité, sans artefacts le long des bords.

`rect= *``*, *``*[, *`coordsizescale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Décalage des pixels du coin supérieur gauche de l’image  du vers le coin supérieur gauche du rectangle  (int, int), exprimé en pixels, après application de l’échelle <span class="varname"></span> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> taille</span> </p></td> 
  <td class="stentry"> <p>Taille du RSI en pixels (int, int). Indique la taille de l’image de réponse. L’image est remplie avec <span class="codeph"> bgc=</span> dans les zones qui ne sont pas couvertes par l’image  (ou est transparente à gauche si <span class="codeph"> fmt=*-alpha</span> est présent dans la requête). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Facteur d’échelle (réel). Les valeurs inférieures à 1,0 réduisent la résolution et les valeurs supérieures à 1,0 augmentent la résolution. </p></td> 
 </tr> 
</table>

Avec cette commande, Image Serving peut diffuser des images volumineuses via HTTP, ce qui dépasserait la taille limite configurée avec `attribute::MaxPix`.

>[!NOTE]
>
>Pour un résultat optimal, lorsque vous utilisez la compression JPEG, la taille de la bande ou de la mosaïque doit être un multiple de la taille de la mosaïque de codage JPEG (16x16 pixels).

## Exemple {#section-932fcfcb41d74a29bc929e4430c49601}

Séparez une image CMJN imprimable en plusieurs bandes pleine résolution afin de réduire la taille des fichiers téléchargés. Si nous devions demander une image contiguë :

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Tout d&#39;abord, des informations pertinentes sur l&#39;image sont obtenues :

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

La réponse textuelle comprend les propriétés suivantes :

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Sur la base de ces informations, nous décidons que nous voulons quatre bandes de 600 x 2 000 pixels. La `rect=` commande sert à décrire les tailles et les positions des bandes.

Comme cette image est fréquemment modifiée, nous inclurons la `id=` commande afin de minimiser les risques que nous obtenions une ou plusieurs bandes d’une ancienne version de l’image qui auraient pu être mises en cache dans un CDN ou un serveur proxy. La valeur de la `image.version` propriété est utilisée à cette fin.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Propriétés {#section-aae223cee13e46d38b74680c048d945b}

attribut . S’applique indépendamment du paramètre de calque actif.

Toutes les zones du RSI qui s’étendent en dehors de l’image  sont complétées par `bgc=`.

Important `rect=` est appliqué *après* la mise à l’échelle finale et l’ajustement avec `scl=`, `wid=`, `hei=`, `fit=`,  et .`rgn=``align=`

## Par défaut {#section-b296d3bbfb19441f87137a452b70f19a}

Image de  entière non modifiée ( `rect=0,0,width,height,1.0`).

## Voir également {#section-74015202c0c545ec82aec614d74b4bbd}

[recadrage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), scl=, align=,fit=, rgn=, attribut de::MaxPix, id=[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
