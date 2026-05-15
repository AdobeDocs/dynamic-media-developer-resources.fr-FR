---
title: ancrage
description: Ancre d’image. Définit le point d’ancrage de l’image, de la couleur unie ou du rectangle du cadre de sélection du texte avant d’appliquer les transformations (recadrage=, échelle=, rotation=, retournement=). Sert également de centre de rotation pour rotation=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
TQID: 'https://experienceleague.adobe.com/GKa8ChLxu85Wmi65uak7Kqn-Kme1GXL0FToaMAgHKoA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 2%

---

# ancrage{#anchor}

Ancre d’image. Définit le point d’ancrage de l’image, de la couleur unie ou du rectangle du cadre de sélection du texte avant d’appliquer les transformations (recadrage=, échelle=, rotation=, retournement=). Sert également de centre de rotation pour rotation=.

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>décalage en pixels par rapport au coin supérieur gauche de l’image source (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>décalage normalisé par rapport au centre de l’image source (réel, réel) </p></td> 
 </tr> 
</table>

Le point d’ancrage est transformé avec l’image et devient le point d’origine du calque (sauf si `origin=` est également spécifié, auquel cas `anchor=` n’est utilisé que comme centre de rotation pour les `rotate=`).

`anchorN=0,0` place l’ancre d’image au centre de l’image source. `anchorN=-0.5,-0.5` ou `anchor=0,0` se trouve dans le coin supérieur gauche et `anchorN=0.5,0.5` dans le coin inférieur droit de l’image source.

## Propriétés {#section-f08942bc6aae46a8b5d341faaff80640}

Attribut d’image Source S’applique au calque actif ou au calque 0, le cas `layer=comp`.

## Par défaut {#section-35d369fab1254f1a9b91684a6e169ad1}

Si `anchor=` n’est pas spécifié, catalog::Anchor est utilisé. Si `catalog::Anchor` n’est pas défini, le centre du rectangle de l’image est utilisé (comme pour spécifier `anchorN=0,0`).

Les calques de texte contenant des `textPs=` et ceux contenant des `clipPath=` peuvent avoir des ancres par défaut différentes.

## Exemple {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Voir « Exemple C » dans [ Modèles ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog::Anchor](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Calques de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
