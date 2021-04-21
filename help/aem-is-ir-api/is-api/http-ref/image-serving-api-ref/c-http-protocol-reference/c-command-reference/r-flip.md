---
description: Retourner la couche. Fait pivoter le calque horizontalement, verticalement ou les deux, après avoir appliqué le paramètre culture= et avant de faire pivoter= et étendre=.
solution: Experience Manager
title: retourner
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# flip{#flip}

Retourner la couche. Fait pivoter le calque horizontalement, verticalement ou les deux, après avoir appliqué le paramètre culture= et avant de faire pivoter= et étendre=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>Retourner le calque horizontalement (de gauche à droite). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>Retourner le calque verticalement (vers le haut). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> rude  </span> </p> </td> 
  <td class="stentry"> <p>Retourner horizontalement et verticalement. </p> </td> 
 </tr> 
</table>

Peut également être appliqué aux calques de texte.

Certaines commandes, dont `extend=`, s’appliquent implicitement au calque 0 au lieu du calque composite lorsque `layer=comp` est sélectionné. Dans ce cas, toutes les commandes attribuées automatiquement à la couche 0 sont appliquées avant les commandes qui s&#39;appliquent à `layer=comp`. Ainsi, lorsque `layer=comp`, `extend=` est appliqué avant `flip=`.

>[!NOTE]
>
>Le calque renversé est positionné en fonction de l’ancrage du calque ; différentes valeurs flip= entraînent des positions de calque différentes lorsque l’ancrage n’est pas situé au centre du calque.

## Propriétés {#section-294da2af7be746b5adfc35e29ee68217}

Calque, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-502044f81a89492198d5f12a738459ea}

Aucune

## Voir aussi {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
