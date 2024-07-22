---
title: direction
description: Indique le mode d’affichage des pages dans la vue principale et les miniatures. Il spécifie également la manière dont l’utilisateur interagit avec l’interface utilisateur de la visionneuse pour changer entre les images de catalogue.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---

# direction{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Indique le mode d’affichage des pages dans la vue principale et les miniatures. Il spécifie également la manière dont l’utilisateur interagit avec l’interface utilisateur de la visionneuse pour changer entre les images de catalogue. </p> <p>Lorsque <span class="codeph"> left </span> est utilisé, il définit un alignement droit pour la page initiale et un alignement gauche pour la dernière page. Elle assemble des sous-images de page individuelles pour l’ordre de rendu de gauche à droite. Il définit également la vue principale pour utiliser l’animation de diapositives de droite à gauche pour faire avancer le catalogue (au cas où <span class="codeph"> PageView.frameTransition </span> serait défini sur diapositive). Enfin, les miniatures sont définies pour un ordre de remplissage de gauche à droite. </p> <p>De même, lorsque <span class="codeph"> à droite </span> est utilisé, il définit un alignement à gauche pour la page initiale et un alignement à droite pour la dernière page. Elle assemble des sous-images de page individuelles pour l’ordre de rendu de droite à gauche. Il définit également la vue principale pour utiliser l’animation des diapositives de gauche à droite pour faire avancer le catalogue (au cas où <span class="codeph"> PageView.frameTransition </span> serait défini sur diapositive). Enfin, l’ordre des miniatures est inversé, de sorte que la vue des miniatures soit renseignée de droite à gauche, de haut en bas. </p> <p>Lorsque <span class="codeph"> auto </span> est défini, la visionneuse applique le mode <span class="codeph"> right </span> lorsque le paramètre régional est défini sur <span class="codeph"> ja ; </span> dans le cas contraire, elle utilise le mode <span class="codeph"> left </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facultatif.

## Par défaut {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Exemple {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
