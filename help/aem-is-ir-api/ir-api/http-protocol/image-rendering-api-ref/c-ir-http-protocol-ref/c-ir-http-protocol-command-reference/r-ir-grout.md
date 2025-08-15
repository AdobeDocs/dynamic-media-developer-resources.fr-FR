---
title: coulis
description: Couleur et épaisseur du coulis de tuile. Simule le coulis pour les carreaux de céramique et de pierre naturelle.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---

# coulis {#grout}

Couleur et épaisseur du coulis de tuile. Simule le coulis pour les carreaux de céramique et de pierre naturelle.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> couleur </span> </span> </p> </td>
  <td class="stentry"> <p>Couleur du coulis (gris ou RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> largeur <span class="varname"> </span> </span> </p> </td>
  <td class="stentry"> <p>Épaisseur du coulis ; unités de coordonnées de la scène (généralement pouces) (réel). </p> </td>
 </tr> 
</table>

Pour un contrôle maximal de l&#39;aspect du coulis, les exigences suivantes s&#39;appliquent :

* La mosaïque doit être carrée ou rectangulaire ; aucune autre forme n&#39;est actuellement prise en charge.
* L’image ne doit contenir qu’une seule mosaïque.
* Le coulis par défaut de l&#39;image (le cas échéant) doit avoir la même épaisseur sur les quatre bords.
* L&#39;épaisseur du coulis par défaut doit être indiquée dans le catalogue des matériaux (`catalog::GroutWidth`).

## Propriétés {#section-de78b678245b4ffda48097c345949e77}

Attribut Material. `*`color`*` Doit être une valeur de couleur RGB. `*`width`*` doit être une valeur réelle égale ou supérieure à 0.

Ignoré si répétition = 4, 5, 7, 8, 9, 14 ou supérieur, ou si spécifié pour des matériaux autres que des textures répétables.

## Par défaut {#section-bfab3621f70b4489a21994ab11b20cc6}

Si `grout=` n’est pas spécifié, le coulis de l’image n’est pas modifié. Si `grout= *`color`*` est spécifié, `*`width`*` est défini par défaut sur `catalog::GroutWidth`.

## Voir aussi {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valeurs de couleur](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
