---
title: Exemple A
description: Créez un modèle de taille fixe avec une image d’arrière-plan statique, une image variable alignée sur l’arrière-plan au centre gauche et mise à l’échelle de manière à ne pas dépasser 80 % de la largeur et de la hauteur de l’arrière-plan. Enfin, un calque de texte avec du texte vertical centré sur le bord droit de la zone de travail.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Exemple A{#example-a}

Créez un modèle de taille fixe avec une image d’arrière-plan statique, une image variable alignée sur l’arrière-plan au centre gauche et mise à l’échelle de manière à ne pas dépasser 80 % de la largeur et de la hauteur de l’arrière-plan. Enfin, un calque de texte avec du texte vertical centré sur le bord droit de la zone de travail.

![Exemple d’image](assets/examplea.png)

## Enregistrement du modèle {#section-32f54710593e438fa0622224c89380af}

Insérer un objet

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogue : Modificateur  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0,5,0&amp;posN=-0,5,0&amp; layer=2&amp;$text=layer+2+text+go=here&amp;text tf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0  </span> </p> </td> 
 </tr> 
</table>

Les valeurs `origin=` de tous les calques sont spécifiées explicitement dans le modèle pour contrôler strictement le positionnement et l’alignement des calques. Chaque origine de calque est définie pour correspondre à l’alignement souhaité pour ce calque. `origin=` pour l’arrière-plan (couche 0) est défini sur le centre ; cette valeur est arbitraire, car l’image d’arrière-plan ne change pas au moment de l’exécution. toute valeur pour l’origine du calque 0 peut être utilisée.

Les valeurs `pos=` fournissent les décalages nécessaires entre les points d’origine du calque, pour obtenir le positionnement souhaité du calque.

L’ancre de l’image du calque 1 est placée au centre gauche, avec la valeur `pos=`. Ce paramètre permet d’obtenir l’alignement gauche entre l’arrière-plan et le calque 1 de l’image, quel que soit le rapport L/H de l’image du calque 1.

De même, l’ancre du calque de texte est positionnée à droite de la zone de texte à taille automatique, avec la valeur `pos=`. Ce paramètre permet d’obtenir l’alignement de centre droit souhaité pour le texte pivoté, indépendamment de la taille de la police et de la longueur des chaînes.

Le texte d’affichage réel est fourni au moment de l’exécution. Par conséquent, une variable est utilisée pour séparer le texte de l’enveloppe de mise en forme rtf. La variable par défaut `$object` est utilisée pour l’image du calque 1. Cette variable vous permet de spécifier cette image dans le chemin de la requête.

Toute image peut être utilisée pour l’image d’arrière-plan et l’image du calque 1. Si l’image d’arrière-plan comporte un masque, les zones non masquées sont remplies avec la couleur d’arrière-plan par défaut ( `attribute::BkgColor`) ou laissées transparentes lorsque `fmt=png-alpha` ou `fmt=tif-alpha`. Si l’image d’arrière-plan a des proportions non carrées, elle est centrée dans l’image de réponse et l’espace supplémentaire est rempli avec `attribute::BkgColor`. Si l’image du calque 1 comporte des données alpha ou un masque, l’image d’arrière-plan (ou couleur d’arrière-plan) reste visible dans les zones transparentes. Si l’image n’a pas de masque, elle remplit l’intégralité du rectangle alloué.

## Utiliser le modèle {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

L’image suivante montre le résultat composite pour différents proportions de l’image du calque 1 et différentes chaînes de texte.

![Exemple Une image composite](assets/exampleausing.png)
