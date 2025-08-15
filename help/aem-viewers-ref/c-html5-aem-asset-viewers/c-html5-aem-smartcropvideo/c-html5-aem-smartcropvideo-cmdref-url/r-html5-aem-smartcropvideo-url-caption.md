---
title: légende
description: Commande d’URL de la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0d7000d0-9181-4c6e-a94e-31ab5ad17fa4
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 5%

---

# légende{#caption}

Commande d’URL de la visionneuse de vidéos avec recadrage intelligent.

` caption= *`fichier`*[,0|1]`

La visionneuse prend en charge le sous-titrage via des fichiers WebVTT hébergés. Les zones géographiques et les indices de chevauchement ne sont pas pris en charge. Les opérateurs de positionnement des repères pris en charge sont les suivants :

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
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>alignement du texte </p> </td> 
   <td colname="col3"> <p><span class="codeph"> gauche|droite|milieu|début|fin</span> </p> </td> 
   <td colname="col4"> <p> Contrôler l’alignement du texte. </p> <p>La valeur par défaut est <span class="codeph"> milieu</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>position du texte </p> </td> 
   <td colname="col3"> <p> 0 % À 100 % </p> </td> 
   <td colname="col4"> <p> Pourcentage d’insertion dans le composant VideoPlayer au début du texte de la légende. </p> <p>La valeur par défaut est 0 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>taille de la ligne </p> </td> 
   <td colname="col3"> <p> 0 % À 100 % </p> </td> 
   <td colname="col4"> <p> Pourcentage de largeur vidéo utilisé pour les sous-titres. </p> <p>La valeur par défaut est de 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>position de la ligne </p> </td> 
   <td colname="col3"> <p> 0%-100%|entier </p> </td> 
   <td colname="col4"> <p> Détermine la position de la ligne sur la page. </p> <p>S’il est exprimé sous la forme d’un entier (pas de signe de pourcentage), il s’agit du nombre de lignes à partir du haut où le texte est affiché. </p> <p>S’il s’agit d’un pourcentage (le signe de pourcentage est le dernier caractère), le texte de la légende est affiché à ce pourcentage dans la zone d’affichage. </p> <p>La valeur par défaut est de 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les autres fonctionnalités WebVTT présentes dans le fichier WebVTT ne sont pas prises en charge, mais ne doivent pas interrompre le sous-titrage.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fichier </span></span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu de légende WebVTT. Traiter le fichier WebVTT par ImageServing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Indique l’état de légende par défaut (activé est <span class="codeph"> 1</span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

Aucune

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
