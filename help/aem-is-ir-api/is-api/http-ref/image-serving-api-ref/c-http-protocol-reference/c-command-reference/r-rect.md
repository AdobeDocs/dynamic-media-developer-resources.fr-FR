---
title: rect
description: Rectangle de vue final. Il permet de démonter l'image de vue finale en plusieurs bandes ou carreaux, qui peuvent être livrés séparément et réassemblés par le client de manière transparente, sans artefacts le long des bords.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
TQID: 'https://experienceleague.adobe.com/v-sAA1KXCiZvFp6NATVZtxYxnQCji3YJZCFa-hcHQYA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 366
ht-degree: 1%

---

# rect{#rect}

Rectangle de vue final. Il permet de démonter l&#39;image de vue finale en plusieurs bandes ou carreaux, qui peuvent être livrés séparément et réassemblés par le client de manière transparente, sans artefacts le long des bords.

`rect= *`coord`*, *`size`*[, *`scale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Décalage en pixels entre le coin supérieur gauche de l’image d’affichage et le coin supérieur gauche du rectangle d’affichage (int, int), exprimé en pixels, après application de <span class="varname">’échelle</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> taille</span> </p></td> 
  <td class="stentry"> <p>Taille du ROI en pixels (int, int). Indique la taille de l’image de réponse. L’image est remplie avec <span class="codeph"> bgc=</span> dans les zones non couvertes par l’image d’affichage (ou laissée transparente, si <span class="codeph"> fmt=*-alpha</span> est présent dans la requête). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> échelle</span> </p></td> 
  <td class="stentry"> <p>Facteur d'échelle (réel). Les valeurs inférieures à 1,0 réduisent la résolution et les valeurs supérieures à 1,0 augmentent la résolution. </p></td> 
 </tr> 
</table>

À l’aide de cette commande, la diffusion d’images peut diffuser des images volumineuses par le biais du protocole HTTP, ce qui dépasserait la limite de taille configurée avec `attribute::MaxPix`.

>[!NOTE]
>
>Pour de meilleurs résultats, lorsque la compression JPEG est utilisée, la taille de la bande ou de la mosaïque doit être un multiple de la taille de la mosaïque de codage JPEG (16 x 16 pixels).

## Exemple {#section-932fcfcb41d74a29bc929e4430c49601}

Séparez une image CMJN imprimable en plusieurs bandes pleine résolution pour réduire la taille des fichiers de téléchargement. Si vous avez demandé une image contiguë :

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Tout d&#39;abord, des informations pertinentes sur l&#39;image sont obtenues :

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

La réponse texte inclut les propriétés suivantes :

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Sur la base de ces informations, quatre bandes de 600x2000 pixels sont souhaitées. La commande `rect=` permet de décrire la taille et la position des bandes.

Cette image étant modifiée fréquemment, la commande `id=` est incluse. Vous minimisez ainsi les risques d’obtenir une ou plusieurs bandes d’une version plus ancienne de l’image qui a pu être mise en cache dans un réseau CDN ou un serveur proxy. La valeur de la propriété `image.version` est utilisée à cet effet.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Propriétés {#section-aae223cee13e46d38b74680c048d945b}

Attribut d’affichage. Il s’applique quel que soit le paramètre de calque actif.

Toutes les zones du retour sur investissement qui s’étendent en dehors de l’image d’affichage sont complétées par des `bgc=`.

Une `rect=` importante est appliquée *après* la mise à l’échelle finale et l’ajustement avec `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` et `align=`.

## Par défaut {#section-b296d3bbfb19441f87137a452b70f19a}

Image d’affichage entière et non modifiée ( `rect=0,0,width,height,1.0`).

## Voir également {#section-74015202c0c545ec82aec614d74b4bbd}

[crops=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
