---
description: Etend le calque. Ajoute des marges sur un calque ou recadre le rectangle du calque.
solution: Experience Manager
title: étendre
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---


# scope{#extend}

Etend le calque. Ajoute des marges sur un calque ou recadre le rectangle du calque.

`extend= *``*, *``*, *``*, *`gauche-droite-droite-droite`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> gauche, haut, bas, droite</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de pixels à ajouter (ou à supprimer de, si la valeur est négative) au bord gauche, supérieur, droit et inférieur du contour du calque (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN, topN, bottomN, rightN</span></span> </p></td> 
  <td class="stentry"> <p>Quantité d’espace à ajouter (ou à supprimer si la valeur est négative) au bord gauche, supérieur, droit et inférieur du rect de calque, exprimée en quantités normalisées par rapport à la taille du rect de calque d’origine (réel, réel, réel, réel). </p></td> 
 </tr> 
</table>

`extend=` est appliquée au calque  ** après le recadrage de l’image (  `crop=`) et toutes les transformations de calque, y compris  `rotate=`, ont été appliquées.

La zone étendue est remplie avec `bgColor=` ou, si elle n’est pas spécifiée, reste transparente.

Les valeurs d’argument de `extendN=` sont normalisées par rapport à la taille du calque rect après les transformations du calque, y compris `rotate=` qui ont été appliquées.

## Propriétés {#section-8fc94de871f841f3bf5e1df135972ca9}

Attribut de couche. S’applique au calque 0 si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, sans modification du rectangle du calque.

## Exemples {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Recadrez une image, puis ajoutez une bordure rouge de 5 pixels de large :**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Applique une échelle de 200 pixels à une image et ajoute le texte de titre dans une marge de 30 pixels au-dessus de l’image.**

Notez que la hauteur de l’image composite varie en fonction des proportions de l’image.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Voir aussi {#section-2d9572be32ca4602b60920b3810f3638}

[recadrage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b),  [origine=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)[
