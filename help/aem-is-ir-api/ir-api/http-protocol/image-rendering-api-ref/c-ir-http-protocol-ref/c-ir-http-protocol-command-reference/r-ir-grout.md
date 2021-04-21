---
description: Couleur et épaisseur du grillage. Simule le grout pour les carreaux de pierre naturelle et céramique.
solution: Experience Manager
title: pâturage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---


# grout{#grout}

Couleur et épaisseur du grillage. Simule le grout pour les carreaux de pierre naturelle et céramique.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>Couleur du sol (gris ou RVB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>Épaisseur du sol ; unités de coordonnées de scène (généralement pouces) (réelles). </p> </td> 
 </tr> 
</table>

Pour un contrôle maximal de l&#39;apparence du grout, les exigences suivantes s&#39;appliquent :

* La mosaïque doit être carrée ou rectangulaire ; pour le moment, aucune autre forme n&#39;est prise en charge.
* L’image ne doit contenir qu’une seule mosaïque.
* Le grain par défaut de l&#39;image (s&#39;il y en a) doit avoir exactement la même épaisseur sur les quatre bords.
* L&#39;épaisseur du grain par défaut doit être spécifiée dans le catalogue de matières ( `catalog::GroutWidth`).

## Propriétés {#section-de78b678245b4ffda48097c345949e77}

Attribut de matériau. `*`La `*` couleur doit être une valeur de couleur RVB. `*`La `*` largeur doit être une valeur réelle de 0 ou plus.

Ignoré si repeat = 4, 5, 7, 8, 9, 14 ou plus, ou si spécifié pour des matières autres que des textures répétables.

## Par défaut {#section-bfab3621f70b4489a21994ab11b20cc6}

Si `grout=` n&#39;est pas spécifié, le grain de l&#39;image n&#39;est pas modifié. Si ` grout= *`color`*` est spécifié, `*`width`*` prend par défaut la valeur `catalog::GroutWidth`.

## Voir aussi {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valeurs de couleur](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
