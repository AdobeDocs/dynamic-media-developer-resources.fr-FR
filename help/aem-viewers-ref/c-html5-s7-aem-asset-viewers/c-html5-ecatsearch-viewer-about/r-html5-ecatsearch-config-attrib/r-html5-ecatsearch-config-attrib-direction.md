---
description: direction
solution: Experience Manager
title: direction
feature: Dynamic Media Classic,Visionneuses,SDK/API,Recherche catalogue électronique
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 3%

---

# direction{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>Indique le mode d’affichage des pages dans la vue principale et les miniatures. Il spécifie également la manière dont l’utilisateur interagit avec l’interface utilisateur de la visionneuse pour changer entre les images de catalogue. </p> <p>Si <span class="codeph"> left </span> est utilisé, il définit un alignement à droite pour la page initiale et un alignement à gauche pour la dernière page. Elle assemble des sous-images de page individuelles pour l’ordre de rendu de gauche à droite. Il définit également la vue principale pour utiliser l’animation des diapositives de droite à gauche afin d’avancer dans le catalogue (au cas où <span class="codeph"> PageView.frametransition </span> serait défini sur diapositive). Enfin, les miniatures sont définies pour un ordre de remplissage de gauche à droite. </p> <p>De même, lorsque <span class="codeph"> droite </span> est utilisé, il définit un alignement à gauche pour la page initiale et un alignement à droite pour la dernière page. Elle assemble des sous-images de page individuelles pour l’ordre de rendu de droite à gauche. Il définit également la vue principale pour utiliser l’animation des diapositives de gauche à droite afin d’avancer dans le catalogue (au cas où <span class="codeph"> PageView.frametransition </span> serait défini sur diapositive). Enfin, l’ordre des miniatures est inversé, de sorte que la vue des miniatures soit renseignée de droite à gauche, de haut en bas. </p> <p>Lorsque <span class="codeph"> auto </span> est défini, la visionneuse applique le <span class="codeph"> droit </span> mode lorsque le paramètre régional est défini sur <span class="codeph"> ja ; </span>sinon, il utilise le mode <span class="codeph"> gauche </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facultatif.

## Par défaut {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Exemple {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
