---
description: Les propriétés de document suivantes sont prises en charge dans les zones de texte.
solution: Experience Manager
title: Propriétés du document (zone de texte)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
TQID: 'https://experienceleague.adobe.com/U8T6F0KmGyopf6rXM0-zssY-hpfKPVUHWt-vO8aA7xM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Propriétés du document (zone de texte){#document-text-box-properties}

Les propriétés de document suivantes sont prises en charge dans les zones de texte.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Commande</b> </th> 
   <th class="entry"> <b> Description </b> </th> 
   <th class="entry"> <b>Notes</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>Tableau des polices. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>Jeu de caractères pour la police <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>Tableau des couleurs de RGB. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>Tableau des couleurs CMJN. </p> </td> 
   <td> <p>Extension Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>Tableau des couleurs pour les couleurs de la diffusion d’images. </p> </td> 
   <td> <p>Extension Dynamic Media ; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>Composant de couleur rouge. </p> </td> 
   <td> <p>Peut apparaître uniquement dans <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vert <span class="varname"> N </span> </span> </td> 
   <td> <p>Composant de couleur verte. </p> </td> 
   <td> <p>Peut apparaître uniquement dans <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \bleu <span class="varname"> N </span> </span> </td> 
   <td> <p>Composant de couleur bleue. </p> </td> 
   <td> <p>Peut apparaître uniquement dans <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan <span class="varname"> N </span> </span> </td> 
   <td> <p>Composant de couleur cyan. </p> </td> 
   <td> <p>Extension Dynamic Media ; peut uniquement apparaître dans <span class="codeph"> \cmykcolortbl </span> ; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>Composant de couleur magenta. </p> </td> 
   <td> <p>Extension Dynamic Media ; peut uniquement apparaître dans <span class="codeph"> \cmykcolortbl </span> ; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \jaune <span class="varname"> N </span> </span> </td> 
   <td> <p>Composant de couleur jaune. </p> </td> 
   <td> <p>Extension Dynamic Media ; peut uniquement apparaître dans <span class="codeph"> \cmykcolortbl </span> ; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \noir <span class="varname"> N </span> </span> </td> 
   <td> <p>Composant de couleur noir. </p> </td> 
   <td> <p>Extension Dynamic Media ; peut uniquement apparaître dans <span class="codeph"> \cmykcolortbl </span> ; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>Marge de gauche. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>Marge de droite. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>Marge du haut. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>Marge du bas. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> uniquement </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>Alignement en haut du texte dans la zone de texte. </p> </td> 
   <td> <p>Par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>Alignement en bas du texte dans la zone de texte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>Centrer le texte dans la zone de texte. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>Orientation du flux de texte. </p> </td> 
   <td> <p>Flux de texte spécifique à la langue ; <span class="codeph"> textPs= </span> uniquement 0 (par défaut) de gauche à droite, de haut en bas (européen) 1 de haut en bas, de droite à gauche (Extrême-Orient) </p> </td> 
  </tr> 
 </tbody> 
</table>
