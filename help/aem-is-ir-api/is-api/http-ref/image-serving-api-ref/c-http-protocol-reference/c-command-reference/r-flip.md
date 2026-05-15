---
title: retourner
description: Retourner le calque. Retourne le calque horizontalement, verticalement ou les deux, après application du recadrage= et avant rotation= et extension=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
TQID: 'https://experienceleague.adobe.com/7RG0rzG40Mp5eQe663S5Ayyf99SIfSLPHgqbSL2Unn4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 2%

---

# retourner{#flip}

Retourner le calque. Retourne le calque horizontalement, verticalement ou les deux, après application du recadrage= et avant rotation= et extension=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Retourner le calque horizontalement (gauche-droite). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Retournez le calque verticalement (vers le haut). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Retourner horizontalement et verticalement. </p> </td> 
 </tr> 
</table>

Il peut également être appliqué aux calques de texte.

Certaines commandes, dont `extend=`, s’appliquent implicitement au calque 0 au lieu du calque composite lorsque `layer=comp` est sélectionné. Dans de tels scénarios, toutes les commandes affectées automatiquement à la couche 0 sont appliquées avant les commandes qui s&#39;appliquent à `layer=comp`. Ainsi, lors de la `layer=comp`, `extend=` est appliquée avant la `flip=`.

>[!NOTE]
>
>La couche inversée est positionnée en fonction de l’ancrage de la couche. Des valeurs de `flip=` différentes entraînent des positions de calque différentes lorsque l’ancre n’est pas au centre du calque.

## Propriétés {#section-294da2af7be746b5adfc35e29ee68217}

Commande Calque. S’applique au calque actif ou à l’image composite, le cas `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-502044f81a89492198d5f12a738459ea}

Aucune

## Voir aussi {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
