---
description: Exigences similaires à celles de l’exemple A, mais utilisez un arrière-plan en couleur unie et laissez la hauteur du composite varier, pour s’adapter à des images avec des proportions différentes.
solution: Experience Manager
title: Exemple B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
TQID: 'https://experienceleague.adobe.com/nwRD9lmoHIjjFR32pdr0g6jRpsIIZicZXmVBXC74ot4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 0%

---

# Exemple B{#example-b}

Exigences similaires à celles de l’exemple A, mais utilisez un arrière-plan en couleur unie et laissez la hauteur du composite varier, pour s’adapter à des images avec des proportions différentes.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

L’image est placée dans le calque 0 et la valeur de hauteur de `size=` est définie sur 0. Ce paramètre fait en sorte que la hauteur réelle soit déterminée par la hauteur de l’image après l’avoir mise à l’échelle sur une largeur de 800 pixels.

La variable `extend=` ajoute 100 pixels en haut et en bas et 200 pixels à droite.

Les origines des calques 0 et 1 sont placées au centre droit de la zone de composition, pour obtenir la position souhaitée du texte.

L’image suivante présente le résultat composite pour différentes proportions de l’image et différentes chaînes de texte.

![Exemple d’image B](assets/exampleb.png)
