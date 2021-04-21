---
description: Image de la carte de l’éclat. Permet de contrôler pixel par pixel la brillance d’une texture, d’un papier peint/bordure répétable ou d’une décale.
solution: Experience Manager
title: glossmap
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---


# glossmap{#glossmap}

Image de la carte de l’éclat. Permet de contrôler pixel par pixel la brillance d’une texture, d’un papier peint/bordure répétable ou d’une décale.

`glossmap={ *``*| *`glossMapFilebeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> imbriquéReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;accolade ;'is&amp;lbrace ;'<span class="varname"> isReq</span>'&amp;rbrace ;'&amp;rbrace ;|&amp;lbrace ;'&amp;lbrace ;'<span class="varname"> foreignReq</span>'&amp;rbrace ;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Fichier image de zone cliquable en niveaux de gris. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Demande au serveur d’images. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>Demande à un serveur étranger. </p></td> 
 </tr> 
</table>

Applicable aux matériaux tels que les effets de peinture métallique, les papiers peints et bordures de papier peint découpé, les tissus de fil métallique, etc.

L’image de zone cliquable brillante doit être en niveaux de gris 8 bits et avoir exactement la même taille que l’image Principale spécifiée avec `src=`. Consultez la description de [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) pour plus d&#39;informations.

## Propriétés {#section-26375672d69849be9b026cc93c3bc558}

Attribut de matériau. Pris en charge par des textures répétables, des papiers peints et des bordures, et des décalcomanies. Ignoré par les matériaux de couleur unie, d&#39;armoire et de garniture de fenêtre. Voir [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) pour plus d&#39;informations.

## Par défaut {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Aucune

## Voir aussi {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
