---
title: rotation
description: Rotation de l’image. Fait pivoter l’image, le texte ou la couche de couleur unie selon l’angle spécifié.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---

# rotation{#rotate}

Rotation de l’image. Fait pivoter l’image, le texte ou la couche de couleur unie selon l’angle spécifié.

`rotate= *`angle`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> angle</span> </p> </td> 
  <td class="stentry"> <p>Angle de rotation en degrés (réel). </p></td> 
 </tr> 
</table>

Les angles positifs tournent dans le sens des aiguilles d&#39;une montre. Le point d’ancrage de calque ( `anchor=` ou `catalog::Anchor`) sert de centre de rotation. Le rectangle du calque est agrandi et ajusté autour des données pivotées selon les besoins pour éviter le recadrage. La rotation est appliquée après le remplissage de la zone d’arrière-plan du calque avec `color=`. Le modificateur `bgColor=` peut être utilisé pour ajouter une couleur d’arrière-plan au rectangle de sélection après la rotation.

## Propriétés {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Couche, commande. S’applique au calque actif ou au calque 0 s’il est `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, sans rotation.

## Exemple {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Placez une étiquette &quot;À la vente&quot; près du coin supérieur gauche des images dans un catalogue d’images. L’image d’étiquette est déjà dimensionnée correctement pour la vue 300x300 et doit être pivotée de 30° vers la gauche. Pour améliorer le libellé, remplissez la zone de texte d’une couleur blanche semi-opaque.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Appliquez `size=` au calque 0 pour définir la taille de l’affichage, plutôt que d’utiliser `wid=` et `hei=`. Cette méthode permet de redimensionner `myImageId` sans modifier la taille finale de `labelImage`. Spécifiez également `scl=1`, sinon l’image composite risque d’être mise à l’échelle sur `attribute::DefaultPix` (sauf si cette valeur est définie sur 0,0). Le modificateur `color=` ajoute la couleur d’arrière-plan semi-opaque à la zone de texte avant la rotation.

L’origine des deux calques est définie dans le coin supérieur gauche pour obtenir l’alignement souhaité. Le point d’origine de la couche 1 s’applique à `labelImage`après sa rotation.

Voir [Exemple A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) pour obtenir un exemple de texte pivoté.

## Voir aussi {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
