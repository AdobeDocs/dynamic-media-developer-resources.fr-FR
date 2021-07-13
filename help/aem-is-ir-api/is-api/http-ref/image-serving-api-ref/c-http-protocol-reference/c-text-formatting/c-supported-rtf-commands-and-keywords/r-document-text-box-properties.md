---
description: Les propriétés de document suivantes sont prises en charge dans les zones de texte.
solution: Experience Manager
title: Propriétés Document (zone de texte)
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---

# Propriétés Document (zone de texte){#document-text-box-properties}

Les propriétés de document suivantes sont prises en charge dans les zones de texte.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Commande</b> </th> 
   <th class="entry"> <b>Description</b> </th> 
   <th class="entry"> <b>Remarques</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl  </span> </td> 
   <td> <p>Tableau de polices. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Jeu de caractères pour la police <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl  </span> </td> 
   <td> <p>Table de couleurs RVB. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>Table de couleurs CMJN. </p> </td> 
   <td> <p>Extension Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>Table de couleurs pour les couleurs de la diffusion d’images. </p> </td> 
   <td> <p>Extension Dynamic Media ; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur rouge. </p> </td> 
   <td> <p>Peut uniquement apparaître dans <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur verte. </p> </td> 
   <td> <p>Peut uniquement apparaître dans <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur bleue. </p> </td> 
   <td> <p>Peut uniquement apparaître dans <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur cyan. </p> </td> 
   <td> <p>Extension Dynamic Media ; ne peut apparaître que dans <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur Magenta. </p> </td> 
   <td> <p>Extension Dynamic Media ; ne peut apparaître que dans <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \jaune  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur jaune. </p> </td> 
   <td> <p>Extension Dynamic Media ; ne peut apparaître que dans <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur noire. </p> </td> 
   <td> <p>Extension Dynamic Media ; ne peut apparaître que dans <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rate  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Marge gauche. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rate  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Marge droite. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rate  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Marge supérieure. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rate  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Marge inférieure. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>Aligne le texte en haut dans la zone de texte. </p> </td> 
   <td> <p>Par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>Aligne le texte en bas dans la zone de texte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc  </span> </td> 
   <td> <p>Centrer le texte dans la zone de texte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Orientation du flux de texte. </p> </td> 
   <td> <p>Flux de texte spécifique à la langue ; <span class="codeph"> textPs= </span> 0 uniquement (par défaut) gauche-droite, haut-bas (européen) 1 haut en bas, droite-gauche (Extrême-Orient) </p> </td> 
  </tr> 
 </tbody> 
</table>
