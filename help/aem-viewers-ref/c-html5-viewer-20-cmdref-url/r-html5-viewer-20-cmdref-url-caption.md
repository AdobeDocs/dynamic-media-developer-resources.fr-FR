---
title: légende
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

# légende{#caption}

Paramètre commun à toutes les visionneuses.

>[!NOTE]
>
>Cette commande ne s’applique pas à la visionneuse d’images vidéo.

` caption= *`lime`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> lime </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu du sous-titrage WebVTT. Image Serving sert le fichier WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Indique l’état par défaut de la légende. Enabled est <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Cette visionneuse prend en charge le sous-titrage codé par le biais de fichiers WebVTT hébergés. Les sous-titres spécifiés avec ce paramètre s’appliquent à la vidéo produite en premier dans les visionneuses de supports ; Les vidéos suivantes sont lues sans sous-titres. Les repères et les régions qui se chevauchent ne sont pas pris en charge. Opérateurs de positionnement de queue pris en charge :

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
   <td colname="col1"> <p> <span class="codeph"> Un </span> </p> </td> 
   <td colname="col2"> <p>Tester l’alignement </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> gauche|droite|milieu|début|fin </span> </p> </td> 
   <td colname="col4"> <p> Contrôle l’alignement du texte. </p> <p>La valeur par défaut est <span class="codeph"> middle </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>Position du texte </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Pourcentage d’insertion dans le composant Lecteur vidéo au début du texte du sous-titre. </p> <p>La valeur par défaut est <span class="codeph"> 0 %. </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>Taille de ligne </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Pourcentage de la largeur de la vidéo utilisée pour les sous-titres. </p> <p>La valeur par défaut est <span class="codeph"> 100 %. </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>Position de la ligne </p> </td> 
   <td colname="col3"> <p> 0 %-100 %|nombre entier </p> </td> 
   <td colname="col4"> <p> Détermine la position de la ligne sur la page. </p> <p>S’il est exprimé sous la forme d’un entier sans signe de pourcentage, il s’agit du nombre de lignes à partir du haut où le texte est affiché. </p> <p>S’il est exprimé en pourcentage - le signe de pourcentage est le dernier caractère - alors le texte de la légende est affiché ce pourcentage dans la zone d’affichage. </p> <p>La valeur par défaut est <span class="codeph"> 100 %. </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Si d’autres fonctionnalités WebVTT sont présentes dans le fichier WebVTT, elles ne sont pas prises en charge ; Toutefois, elles ne perturbent pas le sous-titrage.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> lime </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu de sous-titres WebVTT. Le fichier WebVTT est servi par Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Indique l’état par défaut de la légende. </p> <p>Enabled est <span class="codeph"> 1 </span>. </p> </td> 
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
