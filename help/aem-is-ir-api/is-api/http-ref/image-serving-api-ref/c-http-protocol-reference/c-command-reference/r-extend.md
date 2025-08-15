---
title: étendre
description: Etendre le calque. Ajoute des marges à un calque ou recadre le rectangle du calque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# étendre{#extend}

Etendre le calque. Ajoute des marges à un calque ou recadre le rectangle du calque.

`extend= *`gauche`*, *`, en haut à droite`*, *`en bas`*, *``*`

`extendN= *`gaucheN`*, *`hautN`*, *`droiteN basN`*, *``*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> gauche, haut, bas, droite</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de pixels à ajouter (ou à supprimer, si la valeur est négative) aux bords gauche, supérieur, droit et inférieur du calque rect (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> gaucheN,topN,basN,droiteN</span></span> </p></td> 
  <td class="stentry"> <p>Quantité d’espace à ajouter (ou à supprimer, si la valeur est négative) aux bords gauche, supérieur, droit et inférieur du calque rect, exprimée sous forme de quantités normalisées par rapport à la taille du rect de calque d’origine (réel, réel, réel, réel). </p></td> 
 </tr> 
</table>

`extend=` est appliquée au calque *après* que l’image a été recadrée ( `crop=`) et que toutes les transformations de calque, y compris `rotate=`, ont été appliquées.

La zone étendue est remplie de `bgColor=`ou, si elle n’est pas spécifiée, reste transparente.

Les valeurs des arguments pour `extendN=` sont normalisées par rapport à la taille du calque rect après les transformations de calque, y compris `rotate=` ont été appliquées.

## Propriétés {#section-8fc94de871f841f3bf5e1df135972ca9}

Attribut de calque. S’applique au calque 0 si `layer=comp`. Ignoré par les calques d’effets.

## Par défaut {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, sans modification du rectangle du calque.

## Exemples {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Recadrez une image, puis ajoutez une bordure rouge de 5 pixels de large :**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Redimensionnez une image à une largeur de 200 pixels et ajoutez le texte du titre dans une marge de 30 pixels au-dessus de l’image.**

Notez que la hauteur de l’image composite varie en fonction du format de l’image.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Voir aussi {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
