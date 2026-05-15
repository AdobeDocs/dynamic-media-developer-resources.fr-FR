---
title: Exemple A
description: Créez un modèle à taille fixe avec une image d’arrière-plan statique, une image variable alignée sur l’arrière-plan au centre à gauche et mise à l’échelle pour ne pas dépasser 80 % de la largeur et de la hauteur de l’arrière-plan. Enfin, un calque de texte avec du texte vertical centré sur le bord droit de la zone de travail.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
TQID: 'https://experienceleague.adobe.com/ERioOcY-QrTqAP87kt-ny3XJf-XlbaduI5lXXOHtlgo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 491
ht-degree: 0%

---

# Exemple A{#example-a}

Créez un modèle à taille fixe avec une image d’arrière-plan statique, une image variable alignée sur l’arrière-plan au centre à gauche et mise à l’échelle pour ne pas dépasser 80 % de la largeur et de la hauteur de l’arrière-plan. Enfin, un calque de texte avec du texte vertical centré sur le bord droit de la zone de travail.

![Exemple d’image](assets/examplea.png)

## Enregistrement du modèle {#section-32f54710593e438fa0622224c89380af}

Insérer un objet

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+go+here&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0</span> </p> </td> 
 </tr> 
</table>

Les valeurs `origin=` de tous les calques sont spécifiées explicitement dans le modèle pour contrôler strictement le positionnement et l’alignement des calques. Chaque origine de calque est définie pour correspondre à l’alignement souhaité pour ce calque. La `origin=` de l’arrière-plan (calque 0) est définie sur le centre ; cette valeur est arbitraire, car l’image d’arrière-plan ne change pas au moment de l’exécution ; toute valeur pour l’origine du calque 0 peut être utilisée.

Les valeurs de `pos=` fournissent les décalages nécessaires entre les points d&#39;origine du calque pour obtenir le positionnement de calque souhaité.

L’ancre de l’image du calque 1 est placée au centre gauche, avec la valeur `pos=`. Ce paramètre permet d’aligner l’arrière-plan et l’image du calque 1 sur le centre gauche, quel que soit le format de l’image du calque 1.

De même, l’ancre du calque de texte est positionnée au centre droit de la zone de texte à redimensionnement automatique, avec la valeur `pos=`. Ce paramètre permet d’obtenir l’alignement au centre droit souhaité pour le texte pivoté, quelle que soit la taille de la police et la longueur de la chaîne.

Le texte d’affichage réel est fourni au moment de l’exécution. Une variable est donc utilisée pour séparer le texte de l’enveloppe de formatage rtf. La variable par défaut `$object` est utilisée pour l’image du calque 1. Cette variable vous permet de spécifier cette image dans le chemin d’accès de la requête.

Toute image peut être utilisée pour l’image d’arrière-plan et l’image du calque 1. Si l’image d’arrière-plan comporte un masque, les zones non masquées sont remplies avec la couleur d’arrière-plan par défaut ( `attribute::BkgColor`) ou restent transparentes lorsqu’elles sont `fmt=png-alpha` ou `fmt=tif-alpha`. Si les proportions de l’image d’arrière-plan ne sont pas carrées, elle est centrée dans l’image de réponse et l’espace supplémentaire est rempli de `attribute::BkgColor`. Si l’image du calque 1 contient des données alpha ou un masque, l’image d’arrière-plan (ou la couleur d’arrière-plan) reste visible dans les zones transparentes. Si l’image ne comporte aucun masque, elle remplit l’intégralité du rectangle alloué.

## Utilisation du modèle {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`serveur`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

L’image suivante présente le résultat composite pour différentes proportions de l’image du calque 1 et différentes chaînes de texte.

![Exemple d’image de résultat composite](assets/exampleausing.png)
