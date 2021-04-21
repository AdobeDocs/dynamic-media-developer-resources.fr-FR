---
description: Position du calque.
solution: Experience Manager
title: pos
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---


# pos{#pos}

Position du calque.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Décalage en pixels de l’origine de ce calque à l’origine du calque 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Décalage normalisé de l’origine de ce calque à l’origine du calque 0 (réel, réel). </p></td> 
 </tr> 
</table>

Dans le cas des calques d’image, de texte et de couleur unie, `pos=` indique la position d’un ancrage de calque par rapport à l’ancrage du calque 0. `posN=` les valeurs de coordonnées sont normalisées par rapport à la taille de rect réelle du calque 0.

Dans le cas des calques d’effet, `pos=` déplace le calque d’effet par rapport au calque parent.

Les valeurs positives déplacent le calque vers la droite/le bas, les valeurs négatives vers la gauche/le haut. `posN=0.5,0.5` déplace le calque de la moitié de la largeur et de la hauteur du calque 0 vers le bas et vers la droite.

## Propriétés {#section-51a60cdc52d040538fef378ace7c2e7d}

Attribut de couche. Ignoré si `layer=0` ou `layer=comp`.

## Par défaut {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Ainsi, l’ancre de calque est placée au même emplacement que l’ancre de calque 0 s’il s’agit d’un calque d’image, de texte ou de couleur unie. Positionne un calque d’effets directement sur ou sous son calque parent.

## Exemple {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Voir l&#39;exemple A dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-812d95575ba542808e8387d0a8650606}

[origine=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
