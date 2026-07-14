---
title: opac
description: Opacité. Indique l’opacité du matériau.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
TQID: 'https://experienceleague.adobe.com/j4Y-Lk-BL8VybOYqbP256D81w8FFbQqdS0q8z6Y5l1c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 0%

---

# opac{#opac}

Opacité. Indique l’opacité du matériau.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Opacité du matériau (pourcentage); 0...100 </p> </td> 
 </tr> 
</table>

Les combinaisons matériau/objet suivantes prennent en charge l&#39;opacité variable :

* Couleur unie et textures répétables appliquées aux objets de chevauchement de texture.
* Matériaux de revêtement de fenêtre appliqués à des objets de cadre de revêtement de fenêtre.
* Décalcomanies appliquées aux objets texturaux ou muraux.

Si le matériau comprend une image avec une couche alpha, `opac=` peut être utilisé pour rendre l’image plus transparente, mais pas plus opaque.

## Propriétés {#section-352f7b82ede54159b6afb90ae4b559ec}

Attribut Material. Ignoré si la sélection d&#39;objet en cours ou le matériau ne prend pas en charge l&#39;opacité.

## Par défaut {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, pour un matériau totalement opaque (si l’image ne comprend pas de couche alpha).

