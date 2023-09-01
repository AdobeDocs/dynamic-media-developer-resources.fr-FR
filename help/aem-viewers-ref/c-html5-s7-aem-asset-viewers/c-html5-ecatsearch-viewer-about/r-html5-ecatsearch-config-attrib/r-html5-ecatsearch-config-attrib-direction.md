---
title: direction
description: direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---

# direction{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Indique le mode d’affichage des pages dans la vue principale et les miniatures. Il spécifie également la manière dont l’utilisateur interagit avec l’interface utilisateur de la visionneuse pour changer entre les images de catalogue. </p> <p>When <span class="codeph"> left </span> est utilisé pour définir un alignement à droite pour la page initiale et un alignement à gauche pour la dernière page. Elle assemble des sous-images de page individuelles pour l’ordre de rendu de gauche à droite. Il définit également la vue principale pour utiliser l’animation de diapositives de droite à gauche pour faire avancer le catalogue (au cas où <span class="codeph"> PageView.frameTransition </span> est définie sur diapositive). Enfin, les miniatures sont définies pour un ordre de remplissage de gauche à droite. </p> <p>De même, lorsque <span class="codeph"> right </span> est utilisé pour définir un alignement à gauche pour la page initiale et un alignement à droite pour la dernière page. Elle assemble des sous-images de page individuelles pour l’ordre de rendu de droite à gauche. Il définit également la vue principale afin d’utiliser l’animation des diapositives de gauche à droite pour faire avancer le catalogue (au cas où <span class="codeph"> PageView.frameTransition </span> est définie sur diapositive). Enfin, l’ordre des miniatures est inversé, de sorte que la vue des miniatures soit renseignée de droite à gauche, de haut en bas. </p> <p>When <span class="codeph"> auto </span> est définie, la visionneuse s’applique <span class="codeph"> right </span> mode lorsque le paramètre régional est défini sur <span class="codeph"> ja; </span>sinon, il utilise <span class="codeph"> left </span> mode . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facultatif.

## Par défaut {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Exemple {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
