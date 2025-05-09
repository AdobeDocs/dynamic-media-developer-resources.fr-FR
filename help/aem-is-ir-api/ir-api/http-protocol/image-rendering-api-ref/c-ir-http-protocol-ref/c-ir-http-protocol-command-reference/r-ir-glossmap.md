---
title: glossmap
description: Image de la zone cliquable. Fournit un contrôle pixel par pixel de la brillance d’une texture répétable, du papier peint/de la bordure ou d’un décal.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# glossmap {#glossmap}

Image de la zone cliquable. Fournit un contrôle pixel par pixel de la brillance d’une texture répétable, du papier peint/de la bordure ou d’un décal.

`glossmap={ *`glessMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&location;'is&lbrace;'<span class="varname"> isReq</span>'&brace;'&brace;|&lbrace;'&lbrace;'&lbrace;'<span class="varname"> externalReq</span>'&brace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glessMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Fichier image de la zone cliquable en niveaux de gris. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Demande au serveur d’images. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> étrangerReq </span> </span> </p></td> 
  <td class="stentry"> <p>Demande à un serveur étranger. </p></td> 
 </tr> 
</table>

Applicable aux matériaux tels que les effets de peinture métallique, les papiers peints et bordures en papier découpé et les tissus métalliques.

L’image de la zone cliquable doit être en niveaux de gris 8 bits et avoir la même taille que l’image principale spécifiée avec `src=`. Pour plus d’informations, voir la description de [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) .

## Propriétés {#section-26375672d69849be9b026cc93c3bc558}

Attribut de matière. Pris en charge par les textures répétables, les papiers peints et les bordures, et les décalages. Ignoré par les matériaux de couleur unie, de l’armoire et de la fenêtre. Voir [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) pour plus d’informations.

## Par défaut {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Aucune

## Voir aussi {#section-33953fc1be82452da37141f2e541e00c}

[gless=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
