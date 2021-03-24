---
description: Ancre d’image. Définit le point d’ancrage du rectangle de l’image, de la couleur unie ou du cadre de sélection de texte, avant d’appliquer les transformations (recadrage=, scale=, rotate=, flip=). Sert également de centre de rotation pour rotate=.
solution: Experience Manager
title: ancrage
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---


# ancrage{#anchor}

Ancre d’image. Définit le point d’ancrage du rectangle de l’image, de la couleur unie ou du cadre de sélection de texte, avant d’appliquer les transformations (recadrage=, scale=, rotate=, flip=). Sert également de centre de rotation pour rotate=.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>décalage en pixels à partir du coin supérieur gauche de l’image source (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>décalage normalisé à partir du centre de l’image source (réel, réel) </p></td> 
 </tr> 
</table>

Le point d’ancrage est transformé avec l’image et devient le point d’origine du calque (sauf si `origin=` est également spécifié, auquel cas `anchor=` est utilisé uniquement comme centre de rotation pour `rotate=`).

`anchorN=0,0` place l’ancre d’image au centre de l’image source. `anchorN=-0.5,-0.5` ou  `anchor=0,0` se trouve dans le coin supérieur gauche et  `anchorN=0.5,0.5` se trouve dans le coin inférieur droit de l’image source.

## Propriétés {#section-f08942bc6aae46a8b5d341faaff80640}

Attribut d’image source. S&#39;applique au calque actif ou au calque 0 si `layer=comp`.

## Par défaut {#section-35d369fab1254f1a9b91684a6e169ad1}

Si `anchor=` n&#39;est pas spécifié, catalog::Anchor est utilisé. Si `catalog::Anchor` n’est pas défini, le centre du rectangle de l’image est utilisé (comme si `anchorN=0,0` était spécifié).

Les calques de texte impliquant `textPs=` et les calques impliquant `clipPath=` peuvent avoir des ancres par défaut différentes.

## Exemple {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Voir &quot;Exemple C&quot; dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalogue ::Ancre](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) ,  [origine=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), Calques de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)[
