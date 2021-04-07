---
description: URL de la visionneuse de vidéos interactive.
solution: Experience Manager
title: légende
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéos interactives
role: Développeur, Professionnel
exl-id: 8eb2aa50-52b9-4b63-9789-87e492f34a22
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 10%

---

# caption{#caption}

URL de la visionneuse de vidéos interactive.

` caption= *`file`*[,0|1]`

Le lecteur prend en charge le sous-titrage via des fichiers WebVTT hébergés. Les signaux et les régions qui se chevauchent ne sont pas pris en charge. Les opérateurs de positionnement des indices pris en charge sont les suivants :

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Clé </p> </th> 
   <th colname="col2" class="entry"> <p>Nom </p> </th> 
   <th colname="col3" class="entry"> <p>Valeur </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>alignement de texte </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> gauche|droite|milieu|début|fin  </span> </p> </td> 
   <td colname="col4"> <p> Contrôler l’alignement du texte. </p> <p>La valeur par défaut est <span class="codeph"> mid </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>position du texte </p> </td> 
   <td colname="col3"> <p> 0 à 100 % </p> </td> 
   <td colname="col4"> <p> Pourcentage d’insertion dans le composant VideoPlayer pour le début du texte de la légende. </p> <p>Valeur par défaut : 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>taille de ligne </p> </td> 
   <td colname="col3"> <p> 0 à 100 % </p> </td> 
   <td colname="col4"> <p> Pourcentage de la largeur de vidéo utilisée pour les légendes. </p> <p>Valeur par défaut : 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>position de la ligne </p> </td> 
   <td colname="col3"> <p> 0 %-100 %|entier </p> </td> 
   <td colname="col4"> <p> Détermine la position de la ligne sur la page. </p> <p>S’il est exprimé sous la forme d’un entier (aucun signe de pourcentage), il s’agit du nombre de lignes du haut où le texte est affiché. </p> <p>S’il s’agit d’un pourcentage (le signe pourcentage est le dernier caractère), le texte de la légende s’affiche alors en pourcentage dans la zone d’affichage. </p> <p>Valeur par défaut : 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les autres fonctionnalités WebVTT présentes dans le fichier WebVTT ne sont pas prises en charge, mais ne doivent pas perturber le sous-titrage.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier  </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu de la légende WebVTT. Servez le fichier WebVTT par diffusion d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Indique l’état de légende par défaut (activé est <span class="codeph"> 1 </span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

Aucune

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.caption.vtt,1
```
