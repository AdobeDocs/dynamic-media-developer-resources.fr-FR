---
description: Des exigences similaires telles que l’exemple A, mais qui utilisent un arrière-plan de couleur ferme et permettent à la hauteur du composite de varier, pour s’adapter aux images avec des proportions différentes.
solution: Experience Manager
title: Exemple B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Exemple B{#example-b}

Des exigences similaires telles que l’exemple A, mais qui utilisent un arrière-plan de couleur ferme et permettent à la hauteur du composite de varier, pour s’adapter aux images avec des proportions différentes.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Catalogue <span class="codeph"> ::Id</span> </p> </td> 
  <td class="stentry"> <p>Catalogue <span class="codeph"> ::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extended=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$..rtf-encoding&amp;rotate=-90 originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

L’image est placée dans le calque 0 et la valeur de hauteur de `size=` est définie sur 0. Avec ce paramètre, la hauteur réelle est déterminée par la hauteur de l’image après sa mise à l’échelle à 800 pixels de large.

La variable `extend=` ajoute 100 pixels en haut et en bas, et 200 pixels à droite.

Les origines des calques 0 et 1 sont placées au centre-droit de la zone de composition, afin d’obtenir la position de texte souhaitée.

L’image suivante montre le résultat composite pour différents proportions de l’image et différentes chaînes de texte.

![Exemple B image](assets/exampleb.png)
