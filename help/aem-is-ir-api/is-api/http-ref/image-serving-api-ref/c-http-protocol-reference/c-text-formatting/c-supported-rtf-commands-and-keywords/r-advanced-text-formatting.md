---
description: Utilisez les commandes suivantes pour le formatage avancé du texte.
solution: Experience Manager
title: Formatage de texte avancé
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
TQID: 'https://experienceleague.adobe.com/ZTUWB5N6T-I3DnokCqX--dj9g-807-D9Fv8l20opVkg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 0%

---

# Formatage de texte avancé{#advanced-text-formatting}

Utilisez les commandes suivantes pour le formatage avancé du texte.

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
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>Indice sans modification de la taille de police. </p> </td> 
   <td> <p>Position en demi-points ; la valeur par défaut est 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>Exposant sans modification de la taille de police. </p> </td> 
   <td> <p>Position en demi-points ; la valeur par défaut est 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span> </span> </td> 
   <td> <p>Désactiver/activer à la taille de police spécifiée. </p> </td> 
   <td> <p>Taille de police en demi-points, au-dessus de laquelle appliquer le crénage ; 0 pour désactiver le crénage ; la valeur par défaut est 1 pour le crénage de toutes les tailles de police supérieures à ½ point. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptique </span> </td> 
   <td> <p>Sélectionnez le crénage optique. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>Sélectionnez crénage des mesures. </p> </td> 
   <td> <p>Valeur par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>Modifier l’espacement des caractères. </p> </td> 
   <td> <p>Trimestres positifs ou négatifs ; la valeur par défaut est 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>Modifier l’espacement des caractères. </p> </td> 
   <td> <p>Battements positifs ou négatifs. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>Mise à l’échelle horizontale des caractères. </p> </td> 
   <td> <p>Pourcentage positif ou négatif ; la valeur par défaut est 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>Mise à l’échelle verticale des caractères. </p> </td> 
   <td> <p>Pourcentage positif ou négatif ; la valeur par défaut est 100 ; extension Dynamic Media. </p> <p> <span class="codeph"> \charscaley </span> met également à l'échelle l'interligne lorsqu'il est appliqué avec <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> conserve toujours l’espacement des lignes, quelle que soit la mise à l’échelle verticale des caractères. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Sélectionnez le flux de caractères de gauche à droite. </p> </td> 
   <td> <p>Valeur par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Sélectionnez le flux de caractères de droite à gauche. </p> </td> 
   <td> <p> <span class="codeph"> text= </span> uniquement. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>Activez l’ajustement de copie et définissez la plus grande taille de police autorisée. </p> </td> 
   <td> <p>Taille de police en demi-points ; <span class="codeph"> textPs= </span> uniquement ; extension Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Nombre maximal de lignes d'ajustement (limitation souple). </p> </td> 
   <td> <p>0 pour aucune limitation de ligne ; <span class="codeph"> textPs= </span> uniquement ; extension Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Nombre maximal de lignes de recopie (tronquées). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> uniquement ; extension Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>Orientation des caractères. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> uniquement ; ignoré pour les polices non romaines ; ignoré lorsque <span class="codeph"> \stextflow1 </span> n’est pas en vigueur. </p> <p>0 vertical (par défaut). </p> <p>1 a pivoté de 90 degrés dans le sens des aiguilles d'une montre. </p> </td> 
  </tr> 
 </tbody> 
</table>
