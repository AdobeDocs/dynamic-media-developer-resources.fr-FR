---
description: Commande URL de la visionneuse de vidéos.
solution: Experience Manager
title: caption
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéo
role: Developer,User
exl-id: a9af3335-ae18-4399-9014-47ec0306a087
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 11%

---

# caption{#caption}

Commande URL de la visionneuse de vidéos.

` caption= *`file`*[,0|1]`

La visionneuse prend en charge le sous-titrage codé par le biais de fichiers WebVTT hébergés. Les indicateurs de chevauchement et les régions ne sont pas pris en charge. Les opérateurs de positionnement de repère pris en charge sont les suivants :

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
   <td colname="col2"> <p>alignement de texte </p> </td> 
   <td colname="col3"> <p><span class="codeph"> left|right|middle|start|end</span> </p> </td> 
   <td colname="col4"> <p> Contrôler l’alignement du texte. </p> <p>La valeur par défaut est <span class="codeph"> middle</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>position du texte </p> </td> 
   <td colname="col3"> <p> 0 à 100 % </p> </td> 
   <td colname="col4"> <p> Pourcentage d’insertion dans le composant VideoPlayer pour le début du texte de la légende. </p> <p>Valeur par défaut : 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>taille de ligne </p> </td> 
   <td colname="col3"> <p> 0 à 100 % </p> </td> 
   <td colname="col4"> <p> Pourcentage de la largeur de la vidéo utilisée pour les sous-titres. </p> <p>Valeur par défaut : 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>position ligne </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Détermine la position de la ligne sur la page. </p> <p>S’il est exprimé sous la forme d’un entier (aucun signe de pourcentage), il s’agit du nombre de lignes du haut où le texte est affiché. </p> <p>S’il s’agit d’un pourcentage (le signe de pourcentage est le dernier caractère), le texte de la légende s’affiche avec ce pourcentage dans la zone d’affichage. </p> <p>Valeur par défaut : 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les autres fonctionnalités WebVTT présentes dans le fichier WebVTT ne sont pas prises en charge, mais ne doivent pas perturber le sous-titrage.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> file</span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie une URL ou un chemin d’accès au contenu de la légende WebVTT. Servez le fichier WebVTT par ImageServing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Indique l’état de la légende par défaut (activé est <span class="codeph"> 1</span>). </p> </td> 
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
