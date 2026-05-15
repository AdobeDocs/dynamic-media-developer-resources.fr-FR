---
title: étendre
description: Étendre le calque. Ajoute des marges à un calque ou recadre le rectangle du calque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
TQID: 'https://experienceleague.adobe.com/9toLDEF2GoV-F5J-lxjswISzwgooS4FwqeGF4Gav0tc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 1%

---

# étendre{#extend}

Étendre le calque. Ajoute des marges à un calque ou recadre le rectangle du calque.

`extend= *`gauche`*, *`haut`*, *`droite`*, *`bas`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> gauche, haut, bas, droite</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de pixels à ajouter (ou à supprimer si la valeur est négative) aux bords gauche, supérieur, droit et inférieur du calque rect (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> gaucheN,hautN,basN,droiteN</span></span> </p></td> 
  <td class="stentry"> <p>Quantité d'espace à ajouter (ou à supprimer, si la valeur est négative) aux bords gauche, supérieur, droit et inférieur du calque rect, exprimé en quantités normalisées par rapport à la taille du calque d'origine rect (réel, réel, réel, réel). </p></td> 
 </tr> 
</table>

`extend=` est appliqué au calque *après* l’image est recadrée ( `crop=`) et toutes les transformations de calque, y compris `rotate=`, ont été appliquées.

La zone étendue est remplie de `bgColor=` ou, si elle n&#39;est pas spécifiée, reste transparente.

Les valeurs d&#39;argument pour `extendN=` sont normalisées par rapport à la taille de la couche rect après les transformations de couche, y compris les `rotate=` qui ont été appliquées.

## Propriétés {#section-8fc94de871f841f3bf5e1df135972ca9}

Attribut de calque. S’applique au calque 0 si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, aucune modification du rectangle du calque.

## Exemples {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Recadrez une image, puis ajoutez une bordure rouge de 5 pixels de large :**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Mettez une image à l’échelle sur une largeur de 200 pixels et ajoutez le texte du titre dans une marge de 30 pixels au-dessus de l’image.**

Notez que la hauteur de l’image composite varie en fonction des proportions de l’image.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Voir aussi {#section-2d9572be32ca4602b60920b3810f3638}

[crops=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
