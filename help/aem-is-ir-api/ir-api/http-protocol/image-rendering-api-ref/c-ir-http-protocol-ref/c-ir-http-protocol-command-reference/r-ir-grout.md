---
description: Couleur et épaisseur du carrelage du grout. Simule le grout pour les carreaux de céramique et de pierre naturelle.
seo-description: Couleur et épaisseur du carrelage du grout. Simule le grout pour les carreaux de céramique et de pierre naturelle.
seo-title: grappin
solution: Experience Manager
title: grappin
topic: Scene7 Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# grappin{#grout}

Couleur et épaisseur du carrelage du grout. Simule le grout pour les carreaux de céramique et de pierre naturelle.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> couleur </span></span> </p> </td> 
  <td class="stentry"> <p>Couleur du sol (gris ou RVB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>Epaisseur du sol; unités de coordonnées de scène (généralement pouces) (réel). </p> </td> 
 </tr> 
</table>

Pour un contrôle maximum de l&#39;apparence du grout, les exigences suivantes s&#39;appliquent:

* La mosaïque doit être carrée ou rectangulaire ; pour le moment, aucune autre forme n’est prise en charge.
* L’image ne doit contenir qu’une seule mosaïque.
* Le corps par défaut de l’image (le cas échéant) doit avoir exactement la même épaisseur sur les quatre bords.
* L&#39;épaisseur du grout par défaut doit être spécifiée dans le catalogue de matériaux ( `catalog::GroutWidth`).

## Propriétés {#section-de78b678245b4ffda48097c345949e77}

Attribut de matière. ` *`color`*` doit être une valeur de couleur RVB. ` *`width`*` doit être une valeur réelle de 0 ou plus.

Ignoré si repeat = 4, 5, 7, 8, 9, 14 ou plus, ou si spécifié pour des matières autres que des textures répétables.

## Par défaut {#section-bfab3621f70b4489a21994ab11b20cc6}

S’ `grout=` il n’est pas spécifié, le motif de l’image n’est pas modifié. Si ` grout= *`color`*` est spécifié, la ` *`largeur`*` est définie par défaut sur `catalog::GroutWidth`.

## Voir aussi {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valeurs de couleur](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
