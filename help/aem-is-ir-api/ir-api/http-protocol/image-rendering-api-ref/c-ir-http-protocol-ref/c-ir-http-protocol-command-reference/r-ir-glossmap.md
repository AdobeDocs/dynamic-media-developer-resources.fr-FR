---
title: GlossMap
description: Image de carte brillante. Fournit un contrôle pixel par pixel de la brillance d’une texture, d’un papier peint/bordure ou d’un décalcomanie reproductible.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# GlossMap {#glossmap}

Image de carte brillante. Fournit un contrôle pixel par pixel de la brillance d’une texture, d’un papier peint/bordure ou d’un décalcomanie reproductible.

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace ;' is&amp;lbrace ;'<span class="varname"> isReq</span>'&amp;rbrace ;' &amp;rbrace ;|&amp;lbrace ;' &amp;lbrace ;'<span class="varname"> foreignReq</span>'&amp;rbrace ;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Fichier glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Fichier image de carte brillante (niveaux de gris). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Demande au serveur d’images. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Demande à un serveur étranger. </p></td> 
 </tr> 
</table>

Applicable aux matériaux tels que les effets de peinture métallique, les papiers peints et bordures en papier d’aluminium découpés à l’emporte-pièce et les tissus de fils métalliques.

L’image de gloss map doit être en niveaux de gris 8 bits et avoir la même taille que l’image principale spécifiée avec `src=`. Reportez-vous à la description de [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) pour plus d’informations.

## Propriétés {#section-26375672d69849be9b026cc93c3bc558}

Attribut matériel. Soutenu par des textures reproductibles, des fonds d’écran et des bordures, et des décalcomanies. Ignoré par les matériaux de couleur unie, d’armoire et de couvre-fenêtres. Voir la section [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) pour plus d’informations.

## Par défaut {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Aucune

## Voir aussi {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
