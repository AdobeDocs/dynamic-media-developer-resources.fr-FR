---
title: caption
description: Paramètre commun à toutes les visionneuses.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# caption{#caption}

Paramètre commun à toutes les visionneuses.

>[!NOTE]
>
>Cette commande ne s’applique pas à la visionneuse d’images vidéo.

` caption= *`file`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier </span> </span> </p> </td> 
   <td colname="col2"> <p> Spécifie une URL ou un chemin d’accès au contenu de la légende WebVTT. La diffusion d’images diffuse le fichier WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Indique l’état de la légende par défaut. L’option activée est <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Cette visionneuse prend en charge le sous-titrage par le biais de fichiers WebVTT hébergés. Les sous-titres spécifiés avec ce paramètre s’appliquent à la vidéo qui apparaît en premier dans les visionneuses de médias ; les vidéos suivantes sont lues sans sous-titres. Les indicateurs de chevauchement et les régions ne sont pas pris en charge. Opérateurs de positionnement des repères pris en charge :

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Clé </p> </th> 
   <th colname="col2" class="entry"> <p>Nom </p> </th> 
   <th colname="col3" class="entry"> <p>Valeurs </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>alignement des tests </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end </span> </p> </td> 
   <td colname="col4"> <p> Contrôle l’alignement du texte. </p> <p>La valeur par défaut est <span class="codeph"> middle </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>position du texte </p> </td> 
   <td colname="col3"> <p> 0 à 100 % </p> </td> 
   <td colname="col4"> <p> Pourcentage d’insertion dans le composant VideoPlayer pour le début du texte de la légende. </p> <p>La valeur par défaut est <span class="codeph"> 0 % </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>taille de ligne </p> </td> 
   <td colname="col3"> <p> 0 à 100 % </p> </td> 
   <td colname="col4"> <p> Pourcentage de la largeur de la vidéo utilisée pour les sous-titres. </p> <p>La valeur par défaut est <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>position de ligne </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Détermine la position de la ligne sur la page. </p> <p>S’il est exprimé sous la forme d’un entier sans signe de pourcentage, il s’agit du nombre de lignes du haut où le texte est affiché. </p> <p>S’il est exprimé sous la forme d’un pourcentage (le signe pourcentage est le dernier caractère), le texte de la légende s’affiche sous forme de pourcentage dans la zone d’affichage. </p> <p>La valeur par défaut est <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

S’il existe d’autres fonctionnalités WebVTT présentes dans le fichier WebVTT, elles ne sont pas prises en charge ; toutefois, elles ne perturbent pas le sous-titrage.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier </span> </span> </p> </td> 
   <td colname="col2"> <p> Spécifie une URL ou un chemin d’accès au contenu de la légende WebVTT. Le fichier WebVTT est diffusé par Image Serving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Indique l’état de la légende par défaut. </p> <p>L’option activée est <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif.

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

Aucune

## Exemple {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
