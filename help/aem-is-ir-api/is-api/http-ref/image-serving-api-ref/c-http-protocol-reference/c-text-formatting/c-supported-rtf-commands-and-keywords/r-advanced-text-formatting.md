---
description: Utilisez les commandes suivantes pour un formatage de texte avancé.
solution: Experience Manager
title: Formatage de texte avancé
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Formatage de texte avancé{#advanced-text-formatting}

Utilisez les commandes suivantes pour un formatage de texte avancé.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> Commander </th> 
   <th class="entry"> Description </th> 
   <th class="entry"> Remarques </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>Indice sans modification de la taille de police. </p> </td> 
   <td> <p>Position en demi-points ; La valeur par défaut est 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>Exposant sans modification de la taille de police. </p> </td> 
   <td> <p>Position en demi-points ; La valeur par défaut est 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span> </span> </td> 
   <td> <p>Activer/désactiver à la taille de police spécifiée. </p> </td> 
   <td> <p>Taille de police en demi-points, au-dessus de laquelle appliquer le crénage ; 0 pour désactiver le crénage ; La valeur par défaut est 1 pour le crénage de toutes les tailles de police supérieures à 1/2 point. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningOptique </span> </td> 
   <td> <p>Sélectionnez le crénage optique. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>Sélectionnez le crénage des mesures. </p> </td> 
   <td> <p>Faire défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>Modifier l’espacement des caractères. </p> </td> 
   <td> <p>Quarts de points positifs ou négatifs ; Valeur par défaut : 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>Modifier l’espacement des caractères. </p> </td> 
   <td> <p>Twips positifs ou négatifs. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>Mise à l’échelle horizontale des caractères. </p> </td> 
   <td> <p>Pourcentage positif ou négatif ; La valeur par défaut est 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>Mise à l’échelle verticale des caractères. </p> </td> 
   <td> <p>Pourcentage positif ou négatif ; La valeur par défaut est 100 ; Dynamic Media extension. </p> <p> <span class="codeph"> \charscaley </span> met également à l’échelle l’interligne lorsqu’il est appliqué avec <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> conserve toujours l’interligne quelle que soit la quantité de mise à l’échelle verticale. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Sélectionnez le flux de caractères s’écrivant de gauche à droite. </p> </td> 
   <td> <p>Faire défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Sélectionnez le flux de caractères s’écrivant de droite à gauche. </p> </td> 
   <td> <p> <span class="codeph"> text= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>Activez l’ajustement et définissez la plus grande taille de police autorisée. </p> </td> 
   <td> <p>Taille de police en demi-points ; <span class="codeph"> textPs= </span> only ; Dynamic Media extension. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Lignes d’ajustement maximal (limitation souple). </p> </td> 
   <td> <p>0 pour aucune limitation de ligne ; <span class="codeph"> textPs= </span> only ; Dynamic Media extension. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Lignes d’ajustement maximal (troncations). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only ; Dynamic Media extension. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>Orientation des caractères. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> uniquement ; ignoré pour les polices non romaines ; ignoré lorsque <span class="codeph"> \stextflow1 </span> n’est pas en vigueur. </p> <p>0 verticale (par défaut). </p> <p>1 a pivoté de 90 degrés dans le sens des aiguilles d’une montre. </p> </td> 
  </tr> 
 </tbody> 
</table>
