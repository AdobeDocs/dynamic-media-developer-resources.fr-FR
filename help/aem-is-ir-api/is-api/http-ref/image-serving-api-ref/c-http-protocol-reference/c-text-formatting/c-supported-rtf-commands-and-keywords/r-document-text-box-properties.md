---
description: Les propriétés de document suivantes sont prises en charge dans les zones de texte.
solution: Experience Manager
title: Propriétés de document (zone de texte)
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Propriétés de document (zone de texte){#document-text-box-properties}

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
   <td> <p>Tableau des polices. </p> </td> 
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
   <td> <p>Table de couleurs pour les couleurs de diffusion d’images. </p> </td> 
   <td> <p>Extension Dynamic Media ; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur rouge. </p> </td> 
   <td> <p>Ne peut apparaître que dans <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur verte. </p> </td> 
   <td> <p>Ne peut apparaître que dans <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur bleue. </p> </td> 
   <td> <p>Ne peut apparaître que dans <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant de couleur cyan. </p> </td> 
   <td> <p>Extension Dynamic Media ; ne peut apparaître que dans <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Composant couleur magenta. </p> </td> 
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
   <td> <span class="codeph"> \margl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Marge gauche. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Marge droite. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Marge supérieure. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Marge inférieure. </p> </td> 
   <td> <p>Twips ; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>Aligner le texte en haut dans la zone de texte. </p> </td> 
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
   <td> <p>Orientation de l’enchaînement du texte. </p> </td> 
   <td> <p>Flux de texte spécifique à la langue ; <span class="codeph"> textPs= </span> 0 uniquement (par défaut) gauche-droite, haut-bas (européen) 1 haut en bas, droite-gauche (Extrême-Orient) </p> </td> 
  </tr> 
 </tbody> 
</table>

