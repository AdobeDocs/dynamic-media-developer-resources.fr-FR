---
description: Position du calque.
solution: Experience Manager
title: pos
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
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

En cas de calques d’image, de texte et de couleur uni, `pos=` spécifie la position d’une ancre de calque par rapport à l’ancre de calque 0. `posN=` les valeurs de coordonnée sont normalisées par rapport à la taille réelle de la couche 0 rect.

Dans le cas des calques d’effet, `pos=` déplace la couche d’effet par rapport au calque parent.

Les valeurs positives déplacent le calque vers la droite/le bas, les valeurs négatives vers la gauche/le haut. `posN=0.5,0.5` déplace le calque de la moitié de la largeur et de la hauteur du calque vers le bas et la droite.

## Propriétés {#section-51a60cdc52d040538fef378ace7c2e7d}

Attribut de calque. Ignoré si `layer=0` ou `layer=comp`.

## Par défaut {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Cela place l’ancre de calque au même emplacement que l’ancre de calque 0 s’il s’agit d’une image, d’un texte ou d’un calque de couleur uni. Place un calque d’effet directement sur ou sous son calque parent.

## Exemple {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Voir Exemple A dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
