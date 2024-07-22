---
title: opac
description: Opacité. Spécifie l’opacité du matériau.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# opac{#opac}

Opacité. Spécifie l’opacité du matériau.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>opacité matérielle (pourcentage); 0...100 </p> </td> 
 </tr> 
</table>

Les combinaisons de matériaux/d’objets suivantes prennent en charge une opacité variable :

* Couleur pleine et textures répétables appliquées aux objets de chevauchement de textures.
* Fenêtre recouvrant les matériaux appliqués aux objets de cadre recouvrant la fenêtre.
* Décals appliqués aux objets de texture ou aux objets de mur.

Si la matière contient une image avec un canal alpha, `opac=` peut être utilisé pour rendre l’image plus transparente, mais pas plus opaque.

## Propriétés {#section-352f7b82ede54159b6afb90ae4b559ec}

Attribut de matière. Ignoré si la sélection d’objet actuelle ou la matière ne prend pas en charge l’opacité.

## Par défaut {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, pour un matériau entièrement opaque (si l’image n’inclut pas de canal alpha).
