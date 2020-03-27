---
description: Créez un modèle de taille fixe avec une image d’arrière-plan statique, une image variable alignée avec l’arrière-plan au centre gauche et mise à l’échelle pour ne pas dépasser 80 % de la largeur et de la hauteur de l’arrière-plan, et un calque de texte avec du texte vertical centré sur le bord droit de la zone de travail.
seo-description: Créez un modèle de taille fixe avec une image d’arrière-plan statique, une image variable alignée avec l’arrière-plan au centre gauche et mise à l’échelle pour ne pas dépasser 80 % de la largeur et de la hauteur de l’arrière-plan, et un calque de texte avec du texte vertical centré sur le bord droit de la zone de travail.
seo-title: Exemple A
solution: Experience Manager
title: Exemple A
topic: Scene7 Image Serving - Image Rendering API
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Exemple A{#example-a}

Créez un modèle de taille fixe avec une image d’arrière-plan statique, une image variable alignée avec l’arrière-plan au centre gauche et mise à l’échelle pour ne pas dépasser 80 % de la largeur et de la hauteur de l’arrière-plan, et un calque de texte avec du texte vertical centré sur le bord droit de la zone de travail.

![](assets/examplea.png)

## Enregistrement du modèle {#section-32f54710593e438fa0622224c89380af}

Insérer un objet

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogue:Modificateur </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=arrière-planImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0,5,0&amp;posN=-0,5,0&amp; layer=2&amp;$text=layer+2+text+go+here&amp;text tf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

Les `origin=` valeurs de tous les calques sont spécifiées explicitement dans le modèle pour contrôler strictement le positionnement et l’alignement des calques. Chaque calque   est défini pour correspondre à l’alignement souhaité pour ce calque. Le `origin=` pour l’arrière-plan (calque 0) est défini sur le centre ; c&#39;est arbitraire car l&#39;image d&#39;arrière-plan ne changera pas au moment de l&#39;exécution ; toute valeur pour le 0   peut être utilisée.

Les `pos=` valeurs fournissent les décalages nécessaires entre le calque  les points  du, pour obtenir le positionnement souhaité du calque.

L’ancre de l’image du calque 1 est placée au centre gauche ; conjointement avec la `pos=` valeur, cette option permet d’obtenir l’alignement gauche-centre entre l’image d’arrière-plan et celle du calque 1, quel que soit le rapport L/H de l’image du calque 1.

De même, l’ancre du calque de texte est placée au centre droit de la zone de texte à taille automatique. Conjointement avec pos=, l’alignement souhaité est réalisé au centre droit pour le texte pivoté, indépendamment de la taille de la police et de la longueur de la chaîne.

Le texte d’affichage réel sera fourni lors de l’exécution. Une variable est donc utilisée pour séparer le texte de l’enveloppe de formatage rtf. Nous utilisons la variable par défaut `$object` pour l’image du calque 1. Cela permet de spécifier cette image dans le chemin de requête.

Toute image peut être utilisée pour l’image d’arrière-plan et l’image du calque 1. Si l’image d’arrière-plan comporte un masque, les zones non masquées sont remplies avec la couleur d’arrière-plan par défaut ( `attribute::BkgColor`), ou restent transparentes lorsque `fmt=png-alpha` ou `fmt=tif-alpha`. Si l’image d’arrière-plan présente un format non carré, elle est centrée dans l’image de réponse et l’espace supplémentaire est rempli `attribute::BkgColor`. Si l’image du calque 1 comporte des données alpha ou un masque, l’image d’arrière-plan (ou la couleur d’arrière-plan) reste visible dans les zones transparentes. Si l’image ne comporte aucun masque, elle remplit l’intégralité du rectangle alloué.

## Utilisation du modèle {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

L’illustration suivante montre le résultat composite pour les différents formats de l’image du calque 1 et les différentes chaînes de texte.

![](assets/exampleausing.png)

