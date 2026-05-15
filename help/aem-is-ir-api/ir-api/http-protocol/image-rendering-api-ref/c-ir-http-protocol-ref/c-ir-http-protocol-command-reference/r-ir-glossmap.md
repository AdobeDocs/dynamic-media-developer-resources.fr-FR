---
title: carte lexicale
description: Image de carte brillante. Permet de contrôler pixel par pixel la brillance d’une texture répétable, d’un papier peint/d’une bordure ou d’une vignette.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
TQID: 'https://experienceleague.adobe.com/H-Ip9cbtirNaAhfQwr1lj6T3hYdiD1uG-NdQvCJB1v4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 2%

---

# carte lexicale {#glossmap}

Image de carte brillante. Permet de contrôler pixel par pixel la brillance d’une texture répétable, d’un papier peint/d’une bordure ou d’une vignette.

`glossmap={ *`glossMapFile`*| *`beddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> beddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&lbrace;'is&lbrace;'<span class="varname"> isReq</span>'&rbrace;'&rbrace;|&lbrace;'&lbrace;'<span class="varname"> foreignReq</span>'&rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile </span> </span> </p></td> 
  <td class="stentry"> <p>Fichier image de carte de brillance (niveaux de gris). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Demande au serveur d’images. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Demande à un serveur étranger. </p></td> 
 </tr> 
</table>

Applicable aux matériaux tels que les effets de peinture métallique, les papiers peints et les bordures en aluminium découpés sous pression, et les tissus de fil métallique.

L’image de carte brillante doit être en niveaux de gris 8 bits et avoir la même taille que l’image principale spécifiée par `src=`. Reportez-vous à la description de [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) pour plus d’informations.

## Propriétés {#section-26375672d69849be9b026cc93c3bc558}

Attribut Material. Pris en charge par des textures répétables, des papiers peints et des bordures, et des autocollants. Ignoré par les matériaux de couleur unie, d&#39;armoire et de revêtement de fenêtre. Voir [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) pour plus d’informations.

## Par défaut {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Aucune

## Voir aussi {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
