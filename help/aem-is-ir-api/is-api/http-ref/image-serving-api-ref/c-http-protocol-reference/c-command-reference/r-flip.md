---
title: flip
description: Retourner le calque. Fait pivoter le calque horizontalement, verticalement ou les deux, après avoir appliqué crop= et avant rotate= et extended=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# flip{#flip}

Retourner le calque. Fait pivoter le calque horizontalement, verticalement ou les deux, après avoir appliqué crop= et avant rotate= et extended=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Retourner le calque horizontalement (de gauche à droite). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Retourner le calque verticalement (vers le bas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Symétrie horizontale et verticale. </p> </td> 
 </tr> 
</table>

Elle peut également être appliquée aux calques de texte.

Certaines commandes, notamment `extend=`, s’applique implicitement au calque 0 au lieu du calque composite lors de la `layer=comp` est sélectionnée. Dans ce cas de figure, toutes les commandes attribuées automatiquement à la couche 0 sont appliquées avant les commandes qui s’appliquent à `layer=comp`. Ainsi, lorsque `layer=comp`, `extend=` est appliqué avant `flip=`.

>[!NOTE]
>
>Le calque inversé est positionné en fonction de l’ancrage du calque. Différent `flip=` les valeurs entraînent des positions de calque différentes lorsque l’ancre n’est pas au centre du calque.

## Propriétés {#section-294da2af7be746b5adfc35e29ee68217}

Couche, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-502044f81a89492198d5f12a738459ea}

Aucune

## Voir aussi {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
