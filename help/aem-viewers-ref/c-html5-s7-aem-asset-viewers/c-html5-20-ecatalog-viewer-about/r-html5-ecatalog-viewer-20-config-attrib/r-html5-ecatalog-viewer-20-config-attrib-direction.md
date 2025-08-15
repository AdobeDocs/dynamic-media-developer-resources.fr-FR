---
title: direction
description: Spécifie le mode d’affichage des pages dans la vue principale et les miniatures. Il spécifie également la façon dont l’utilisateur interagit avec l’interface utilisateur de la visionneuse pour passer d’un cadre de catalogue à l’autre.
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
   <td colname="col1"> <p> <span class="codeph"> auto|gauche|droite </span> </p> </td> 
   <td colname="col2"> <p>Spécifie le mode d’affichage des pages dans la vue principale et les miniatures. Il spécifie également la façon dont l’utilisateur interagit avec l’interface utilisateur de la visionneuse pour passer d’un cadre de catalogue à l’autre. </p> <p>Lorsque <span class="codeph"> l’option gauche </span> est utilisée, elle définit un alignement à droite pour la page initiale et à gauche pour la dernière page. Il assemble les sous-images de page individuelles dans l’ordre de rendu de gauche à droite. Il définit également la vue principale pour utiliser l’animation de diapositive de droite à gauche pour avancer le catalogue (au cas où <span class="codeph"> PageView.frametransition </span> est défini sur glissement). Enfin, les vignettes sont définies pour un ordre de remplissage de gauche à droite. </p> <p>De même, lorsque <span class="codeph"> la droite </span> est utilisée, elle définit un alignement à gauche pour la page initiale et à droite pour la dernière page. Il assemble les sous-images de page individuelles dans l’ordre de rendu de droite à gauche. Il définit également la vue principale pour utiliser l’animation de diapositive de gauche à droite pour avancer le catalogue (au cas où <span class="codeph"> PageView.frametransition </span> est défini sur glissement). Enfin, il inverse l’ordre des vignettes afin que la vue des miniatures soit remplie de droite à gauche, de haut en bas. </p> <p>Lorsque <span class="codeph"> la valeur automatique </span> est définie, la visionneuse applique <span class="codeph"> le mode droit </span> lorsque les paramètres régionaux sont définis sur <span class="codeph"> ja ; </span>Sinon, il utilise <span class="codeph"> le mode gauche </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facultatif.

## Par défaut {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Exemple {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
