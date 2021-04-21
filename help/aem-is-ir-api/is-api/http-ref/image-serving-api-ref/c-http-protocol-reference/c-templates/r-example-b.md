---
description: Des exigences similaires telles que l’exemple A, mais utilisent un arrière-plan de couleur unie et permettent à la hauteur du composite de varier, pour s’adapter aux images présentant des proportions différentes.
solution: Experience Manager
title: Exemple B
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Exemple B{#example-b}

Des exigences similaires telles que l’exemple A, mais utilisent un arrière-plan de couleur unie et permettent à la hauteur du composite de varier, pour s’adapter aux images présentant des proportions différentes.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalogue : Modificateur</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+going+here&amp; layer=0&amp;size=800,0&amp;extended=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf..$text$..rtf-encoding&amp;rotate=-90&amp;origin=.5,0&amp;posN=0,5,0</span> </p></td> 
 </tr> 
</table>

L’image est placée dans le calque 0 et la valeur de hauteur `size=` est définie sur 0, ce qui fait que la hauteur réelle est déterminée par la hauteur de l’image après sa mise à l’échelle avec une largeur de 800 pixels.

`extend=` ajoute 100 pixels en haut et en bas et 200 pixels à droite.

Les origines des calques 0 et 1 sont placées au centre-droit de la zone de composition pour obtenir la position souhaitée du texte.

L’illustration suivante montre le résultat composite pour les différents formats de l’image et les différentes chaînes de texte.

![](assets/exampleb.png)

