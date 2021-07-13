---
description: Utilisez les commandes suivantes pour la mise en forme de texte avancée.
solution: Experience Manager
title: Formatage de texte avancé
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---

# Formatage de texte avancé{#advanced-text-formatting}

Utilisez les commandes suivantes pour la mise en forme de texte avancée.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> Commande </th> 
   <th class="entry"> Description </th> 
   <th class="entry"> Remarques </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Indice sans changement de taille de police. </p> </td> 
   <td> <p>position en demi-points; La valeur par défaut est 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Exposant sans changement de taille de police. </p> </td> 
   <td> <p>position en demi-points; La valeur par défaut est 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Désactivez/activez à la taille de police spécifiée. </p> </td> 
   <td> <p>Taille de police en demi-points, au-dessus de laquelle appliquer le crénage ; 0 pour désactiver le crénage ; La valeur par défaut est 1 pour le crénage de toutes les tailles de police sur un demi-point. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptique  </span> </td> 
   <td> <p>Sélectionnez le crénage optique. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric  </span> </td> 
   <td> <p>Sélectionnez le crénage des mesures. </p> </td> 
   <td> <p>Par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \développer  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Modifier l’espacement des caractères </p> </td> 
   <td> <p>des points de quart positifs ou négatifs ; La valeur par défaut est 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \extensiontw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Modifier l’espacement des caractères </p> </td> 
   <td> <p>Des twips positives ou négatives. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Mise à l’échelle horizontale des caractères. </p> </td> 
   <td> <p>Pourcentage positif ou négatif ; la valeur par défaut est 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Mise à l’échelle verticale des caractères. </p> </td> 
   <td> <p>Pourcentage positif ou négatif ; la valeur par défaut est 100 ; Extension Dynamic Media. </p> <p> <span class="codeph"> \charscaley met  </span> également à l’échelle l’interligne lorsqu’il est appliqué avec  <span class="codeph"> text=  </span>. <span class="codeph"> textPs= conserve  </span> toujours l’interligne, quelle que soit la mise à l’échelle verticale des caractères. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>Sélectionnez le flux de caractères de gauche à droite. </p> </td> 
   <td> <p>Par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>Sélectionnez le flux de caractères de droite à gauche. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Activez l’ajustement de copie et définissez la taille de police autorisée la plus grande. </p> </td> 
   <td> <p>Taille de police en demi-points ; <span class="codeph"> textPs= </span> uniquement ; Extension Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Nombre maximal de lignes ajustées à la copie (limite souple). </p> </td> 
   <td> <p>0 sans limite de ligne ; <span class="codeph"> textPs= </span> uniquement ; Extension Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Nombre maximal de lignes ajustées à la copie (tronquage). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> uniquement; Extension Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Orientation du caractère. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> uniquement; ignoré pour les polices non romaines ; ignoré lorsque  <span class="codeph"> \stextflow1  </span> n’est pas en vigueur. </p> <p>0 vertical (par défaut). </p> <p>1 a pivoté de 90 degrés dans le sens des aiguilles d’une montre. </p> </td> 
  </tr> 
 </tbody> 
</table>
