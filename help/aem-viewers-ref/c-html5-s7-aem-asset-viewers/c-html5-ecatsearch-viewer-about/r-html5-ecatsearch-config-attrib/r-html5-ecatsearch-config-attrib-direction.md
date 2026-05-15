---
title: direction
description: direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
TQID: 'https://experienceleague.adobe.com/tNKu0P8Sgoxas-opiWd1GWkuWYWDfXE0-j1A-p-j-jM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 206
ht-degree: 2%

---

# direction{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|gauche|droite </span> </p> </td> 
   <td colname="col2"> <p>Indique le mode d’affichage des pages dans la vue principale et les miniatures. Elle spécifie également la manière dont l’utilisateur interagit avec l’interface utilisateur de la visionneuse pour passer d’un cadre de catalogue à un autre. </p> <p>Lorsque <span class="codeph">’</span> de gauche est utilisé, il définit un alignement à droite pour la page initiale et un alignement à gauche pour la dernière page. Il regroupe des sous-images de page individuelles pour un ordre de rendu de gauche à droite. Il définit également la vue principale de sorte à utiliser l'animation de diapositives de droite à gauche pour faire avancer le catalogue (dans le cas où <span class="codeph"> pageView.frametransition </span> est définie sur diapositive). Enfin, les miniatures sont définies dans un ordre de remplissage de gauche à droite. </p> <p>De même, lorsque <span class="codeph">’</span> de droite est utilisé, il définit un alignement à gauche pour la page initiale et un alignement à droite pour la dernière page. Il regroupe des sous-images de page individuelles pour un ordre de rendu de droite à gauche. Il définit également la vue principale de sorte que l'animation des diapositives s'effectue de gauche à droite pour faire avancer le catalogue (si <span class="codeph">'</span> PageView.frametransition est définie sur diapositive). Enfin, l’ordre des miniatures est inversé, de sorte que la vue des miniatures est renseignée de droite à gauche, de haut en bas. </p> <p>Lorsque <span class="codeph"> paramètre </span> automatique est défini, la visionneuse applique <span class="codeph"> mode de </span> de droite lorsque le paramètre régional est défini sur <span class="codeph"> ja ; </span>dans le cas contraire, elle utilise <span class="codeph"> mode de </span> de gauche. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facultatif.

## Par défaut {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Exemple {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
