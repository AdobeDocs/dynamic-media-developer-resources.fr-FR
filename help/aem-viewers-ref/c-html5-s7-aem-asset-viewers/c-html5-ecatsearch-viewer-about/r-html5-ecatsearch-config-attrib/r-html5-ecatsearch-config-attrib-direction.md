---
description: 'null'
seo-description: 'null'
seo-title: direction
solution: Experience Manager
title: direction
topic: Dynamic media
uuid: 0a30f3b0-64c8-4799-b4f5-fc8996a8b5a4
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# direction{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Indique le mode d’affichage des pages dans le  principal et dans les vignettes. Il indique également la manière dont l’utilisateur interagit avec l’interface utilisateur du lecteur de contenu pour changer d’un bloc de catalogue à l’autre. </p> <p>Lorsqu’ <span class="codeph"> elle est utilisée, </span> elle définit un alignement à droite pour la page initiale et un alignement à gauche pour la dernière page. Elle stimule des sous-images de page individuelles pour l’ordre de rendu de gauche à droite. Il permet également au principal d’utiliser l’animation de diapositives de droite à gauche pour faire avancer le catalogue (au cas où <span class="codeph"> PageView.frametransition </span> serait définie sur Diapositive). Enfin, les vignettes sont définies pour un ordre de remplissage de gauche à droite. </p> <p>De même, lorsque <span class="codeph"> la droite </span> est utilisée, elle définit un alignement à gauche pour la page initiale et un alignement à droite pour la dernière page. Elle stimule des sous-images de page individuelles pour un ordre de rendu de droite à gauche. Il permet également au principal d’utiliser l’animation des diapositives de gauche à droite pour faire avancer le catalogue (au cas où <span class="codeph"> PageView.frametransition </span> serait définie sur Diapositive). Enfin, il inverse l’ordre des miniatures afin que le  des miniatures soit rempli de droite à gauche, de haut en bas. </p> <p>Lorsque l’option <span class="codeph"> auto </span> est définie, le lecteur applique le <span class="codeph"> bon </span> mode lorsque le paramètre régional est défini sur <span class="codeph"> ja ; </span>dans le cas contraire, il utilise le mode <span class="codeph"> gauche </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facultatif.

## Par défaut {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Exemple {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
