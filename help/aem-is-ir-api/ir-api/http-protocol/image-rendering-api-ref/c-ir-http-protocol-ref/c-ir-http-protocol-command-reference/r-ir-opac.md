---
description: Opacité. Indique l’opacité du matériau.
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 7910228217db2c97dccd306ce464c69da53ee576
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# opac{#opac}

Opacité. Indique l’opacité du matériau.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>opacité du matériau (en pourcentage); 0...100 </p> </td> 
 </tr> 
</table>

Les combinaisons matériau/objet suivantes prennent en charge l’opacité variable :

* Couleur unie et textures répétables appliquées aux objets de chevauchement de textures.
* Fenêtre recouvrant les matériaux appliqués aux objets de cadre de recouvrement de fenêtre.
* Reflet appliqué aux objets texturaux ou aux objets muraux.

Si le matériau contient une image avec un canal alpha, `opac=` peut être utilisé pour rendre l&#39;image plus transparente, mais pas plus opaque.

## Propriétés {#section-352f7b82ede54159b6afb90ae4b559ec}

Attribut de matériau. Ignoré si la sélection d’objet ou la matière active ne prend pas en charge l’opacité.

## Par défaut {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, pour un matériau entièrement opaque (si l&#39;image n&#39;inclut pas de canal alpha).
