---
title: rotation
description: Faire pivoter l’image. Fait pivoter le calque d’image, de texte ou de couleur unie selon l’angle spécifié.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
TQID: 'https://experienceleague.adobe.com/WDC8SRJEBqspJidlNPxLvwmX-HMQG1zC6wwHNJIXLK4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 2%

---

# rotation{#rotate}

Faire pivoter l’image. Fait pivoter le calque d’image, de texte ou de couleur unie selon l’angle spécifié.

`rotate= *` angle `*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> angle</span> </p> </td> 
  <td class="stentry"> <p>Angle de rotation en degrés (réel). </p></td> 
 </tr> 
</table>

Les angles positifs tournent dans le sens des aiguilles d&#39;une montre. Le point d’ancrage du calque (`anchor=` ou `catalog::Anchor`) sert de centre de rotation. Le rectangle de calque est agrandi et ajusté autour des données pivotées selon les besoins pour éviter le recadrage. La rotation est appliquée après le remplissage de la zone d&#39;arrière-plan du calque avec `color=`. Le modificateur `bgColor=` peut être utilisé pour ajouter une couleur de fond au rectangle englobant après la rotation.

## Propriétés {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Commande Calque. S’applique au calque actif ou au calque 0, le cas `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, pas de rotation.

## Exemple {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Placez un libellé « En vente » près du coin supérieur gauche des images dans un catalogue d’images. L’image du libellé est déjà dimensionnée correctement pour la vue 300x300 et doit pivoter de 30° vers la gauche. Pour rehausser le libellé, remplissez la zone de texte avec une couleur blanche semi-opaque.

`http:// *`serveur`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Appliquez des `size=` au calque 0 pour définir la taille d&#39;affichage, plutôt que d&#39;utiliser `wid=` et `hei=`. Cette méthode permet de redimensionner les `myImageId` sans modifier la taille finale des `labelImage`. Indiquez également `scl=1`, sinon l’image composite peut être mise à l’échelle sur `attribute::DefaultPix` (sauf si elle est définie sur 0,0). Le modificateur `color=` ajoute la couleur d’arrière-plan semi-opaque à la zone de texte avant la rotation.

L’origine des deux calques est définie dans le coin supérieur gauche pour obtenir l’alignement souhaité. Le point d&#39;origine du calque 1 s&#39;applique à `labelImage`après sa rotation.

Voir [Exemple A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) pour un exemple de texte pivoté.

## Voir aussi {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
