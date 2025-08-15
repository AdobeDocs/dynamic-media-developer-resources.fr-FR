---
description: Exigences similaires à celles de l’exemple A, mais utilisez un arrière-plan de couleur unie et laissez la hauteur du composite varier, pour s’adapter aux images avec différents rapports d’aspect.
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

Exigences similaires à celles de l’exemple A, mais utilisez un arrière-plan de couleur unie et laissez la hauteur du composite varier, pour s’adapter aux images avec différents rapports d’aspect.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog ::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog ::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$... rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

L’image est placée dans le calque 0 et la hauteur de `size=` est définie sur 0. Ce paramètre détermine la hauteur réelle par la hauteur de l’image après l’avoir mise à l’échelle à 800 pixels de large.

La variable `extend=` ajoute 100 pixels en haut et en bas, et 200 pixels à droite.

Les origines du calque 0 et du calque 1 sont placées au centre-droit de la zone de composition, pour obtenir la position de texte souhaitée.

L’image suivante montre le résultat composite pour différents rapports d’aspect de l’image et différentes chaînes de texte.

![Exemple d’image B](assets/exampleb.png)
