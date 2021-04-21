---
description: direction
solution: Experience Manager
title: direction
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---


# direction{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>Indique le mode d’affichage des pages dans la vue principale et les miniatures. Il indique également comment l’utilisateur interagit avec l’interface utilisateur du lecteur de contenu pour changer d’un bloc de catalogue à l’autre. </p> <p>Lorsque <span class="codeph"> left </span> est utilisé, il définit un alignement à droite pour la page initiale et un alignement à gauche pour la dernière page. Il sélectionne des sous-images de page individuelles pour l’ordre de rendu de gauche à droite. Il définit également la vue principale pour utiliser l'animation de diapositives de droite à gauche pour faire avancer le catalogue (au cas où <span class="codeph"> PageView.frametransition </span> serait définie sur diapositive). Enfin, les miniatures sont définies pour un ordre de remplissage de gauche à droite. </p> <p>De même, lorsque <span class="codeph"> right </span> est utilisé, il définit un alignement à gauche pour la page initiale et un alignement à droite pour la dernière page. Il sélectionne des sous-images de page individuelles pour un ordre de rendu de droite à gauche. Il définit également la vue principale d'utilisation de l'animation de diapositives de gauche à droite pour faire avancer le catalogue (au cas où <span class="codeph"> PageView.frametransition </span> serait définie sur diapositive). Enfin, elle inverse l’ordre des miniatures afin que la vue des miniatures soit remplie de droite à gauche, de haut en bas. </p> <p>Lorsque <span class="codeph"> auto </span> est défini, le lecteur applique le mode <span class="codeph"> right </span> lorsque le paramètre régional est défini sur <span class="codeph"> ja; </span>sinon, il utilise le mode <span class="codeph"> left </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facultatif.

## Par défaut {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Exemple {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
