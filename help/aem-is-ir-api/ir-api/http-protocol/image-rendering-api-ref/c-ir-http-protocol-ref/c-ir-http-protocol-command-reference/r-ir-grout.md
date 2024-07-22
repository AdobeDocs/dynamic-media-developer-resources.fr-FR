---
title: grout
description: Couleur et épaisseur du sol en mosaïque. Simule le grout pour les tuiles en céramique et en pierre naturelle.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---

# grout {#grout}

Couleur et épaisseur du sol en mosaïque. Simule le grout pour les tuiles en céramique et en pierre naturelle.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td>
  <td class="stentry"> <p>Couleur du sol (gris ou RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>Epaisseur du sol ; unités de coordonnées de scène (généralement pouces) (réelles). </p> </td>
 </tr> 
</table>

Pour un contrôle maximal de l’apparence du groupe, les exigences suivantes s’appliquent :

* La mosaïque doit être carrée ou rectangulaire ; aucune autre forme n’est actuellement prise en charge.
* L’image ne doit contenir qu’une seule mosaïque.
* Le motif par défaut de l’image (le cas échéant) doit avoir la même épaisseur sur les quatre bords.
* L&#39;épaisseur du sol par défaut doit être spécifiée dans le catalogue de matériaux ( `catalog::GroutWidth`).

## Propriétés {#section-de78b678245b4ffda48097c345949e77}

Attribut de matière. `*`color`*` Doit être une valeur de couleur RGB. `*`width`*` doit être une valeur réelle de 0 ou supérieure.

Ignoré si repeat = 4, 5, 7, 8, 9, 14 ou supérieur, ou lorsqu’il est spécifié pour des matières autres que des textures répétables.

## Par défaut {#section-bfab3621f70b4489a21994ab11b20cc6}

Si `grout=` n’est pas spécifié, le grain de l’image n’est pas modifié. Si `grout= *`color`*` est spécifié, `*`width`*` est défini par défaut sur `catalog::GroutWidth`.

## Voir aussi {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valeurs de couleur](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
