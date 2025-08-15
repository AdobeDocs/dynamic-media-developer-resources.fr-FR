---
title: légende
description: URL de la visionneuse de vidéo interactive.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 8eb2aa50-52b9-4b63-9789-87e492f34a22
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 3%

---

# légende{#caption}

URL de la visionneuse de vidéo interactive.

` caption= *`lime`*[,0|1]`

La visionneuse prend en charge le sous-titrage codé via des fichiers WebVTT hébergés. Les repères et les régions qui se chevauchent ne sont pas pris en charge. Les opérateurs de positionnement de repères pris en charge sont les suivants :

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
   <td colname="col1"> <p> <span class="codeph"> Un </span> </p> </td> 
   <td colname="col2"> <p>Alignement du texte </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> gauche|droite|milieu|début|fin </span> </p> </td> 
   <td colname="col4"> <p> Contrôle de l’alignement du texte. </p> <p>La valeur par défaut est <span class="codeph"> middle </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>Position du texte </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Pourcentage d’insertion dans le composant Lecteur vidéo au début du texte du sous-titre. </p> <p>La valeur par défaut est 0 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>Taille de ligne </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Pourcentage de la largeur de la vidéo utilisée pour les sous-titres. </p> <p>La valeur par défaut est 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>Position de la ligne </p> </td> 
   <td colname="col3"> <p> 0 %-100 %|nombre entier </p> </td> 
   <td colname="col4"> <p> Détermine la position de la ligne sur la page. </p> <p>S’il est exprimé sous la forme d’un entier (sans signe de pourcentage), il s’agit du nombre de lignes à partir du haut où le texte est affiché. </p> <p>S’il s’agit d’un pourcentage (le signe de pourcentage est le dernier caractère), le texte de la légende est affiché ce pourcentage dans la zone d’affichage. </p> <p>La valeur par défaut est 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les autres fonctionnalités WebVTT présentes dans le fichier WebVTT ne sont pas prises en charge, mais ne doivent pas perturber le sous-titrage.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> lime </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu du sous-titrage WebVTT. Présentez le fichier WebVTT par l’hébergeur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Indique l’état par défaut de la légende (l’option est <span class="codeph"> 1 </span>). </p> </td> 
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
