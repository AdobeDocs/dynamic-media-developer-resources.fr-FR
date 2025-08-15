---
title: Exemple A
description: Créez un modèle de taille fixe avec une image d’arrière-plan statique, une image variable alignée sur l’arrière-plan au centre gauche et mise à l’échelle pour ne pas dépasser 80 % de la largeur et de la hauteur de l’arrière-plan. Enfin, un calque de texte avec du texte vertical centré sur le bord droit de la zone de travail.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Exemple A{#example-a}

Créez un modèle de taille fixe avec une image d’arrière-plan statique, une image variable alignée sur l’arrière-plan au centre gauche et mise à l’échelle pour ne pas dépasser 80 % de la largeur et de la hauteur de l’arrière-plan. Enfin, un calque de texte avec du texte vertical centré sur le bord droit de la zone de travail.

![Exemple Une image](assets/examplea.png)

## L’enregistrement du modèle {#section-32f54710593e438fa0622224c89380af}

Insérer l’objet

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog ::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monModèle1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog ::Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+goes+here&amp;text=rtf...$text$... rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

Les `origin=` valeurs de tous les calques sont spécifiées explicitement dans le modèle pour contrôler strictement le positionnement et l’alignement des calques. L’origine de chaque calque est définie pour correspondre à l’alignement souhaité pour ce calque. La `origin=` valeur de l’arrière-plan (calque 0) est définie sur le centre ; cette valeur est arbitraire car l’image d’arrière-plan ne change pas au moment de l’exécution ; n’importe quelle valeur pour l’origine du calque 0 peut être utilisée.

Les `pos=` valeurs fournissent les décalages nécessaires entre les points d’origine de la couche, pour obtenir le positionnement de couche souhaité.

L’ancrage de l’image du calque 1 est placé au centre gauche, avec la `pos=` valeur. Ce paramètre permet d’obtenir l’alignement au centre gauche entre l’arrière-plan et l’image du calque 1, quel que soit le format de l’image du calque 1.

De même, l’ancre du calque de texte est positionnée au centre droit de la zone de texte à dimensionnement automatique, avec la `pos=` valeur. Ce paramètre permet d’obtenir l’alignement au centre à droite souhaité pour le texte pivoté, indépendamment de la taille de la police et de la longueur de la chaîne.

Le texte d’affichage réel est fourni au moment de l’exécution, de sorte qu’une variable est utilisée pour séparer le texte de l’enveloppe de formatage rtf. La variable `$object` par défaut est utilisée pour l’image du calque 1. Cette variable permet de spécifier cette image dans le chemin d’accès à la demande.

N’importe quelle image peut être utilisée pour l’image d’arrière-plan et l’image de calque 1. Si l’image d’arrière-plan comporte un masque, les zones non masquées sont remplies avec la couleur d’arrière-plan par défaut ( `attribute::BkgColor`), ou laissées transparentes lorsque `fmt=png-alpha` ou `fmt=tif-alpha`. Si l’image d’arrière-plan a un rapport d’aspect non carré, elle est centrée dans l’image de réponse et l’espace supplémentaire est rempli avec `attribute::BkgColor`. Si l’image du calque 1 contient des données alpha ou un masque, l’image d’arrière-plan (ou la couleur d’arrière-plan) reste visible dans les zones transparentes. Si l’image ne comporte pas de masque, elle remplit la totalité du rectangle alloué.

## Utilisation du modèle {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`serveur`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

L’image suivante montre le résultat composite pour différents rapports d’aspect de l’image de couche 1 et différentes chaînes de texte.

![Exemple : Image de résultat composite](assets/exampleausing.png)
