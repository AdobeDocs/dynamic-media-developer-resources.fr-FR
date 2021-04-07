---
description: Paramètre commun à toutes les visionneuses.
solution: Experience Manager
title: légende
feature: Dynamic Media Classic, Visionneuses, SDK/API
role: Développeur, Professionnel
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 6%

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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier  </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu de la légende WebVTT. Image Serving diffuse le fichier WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Indique l’état de légende par défaut. Activé est <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ce lecteur prend en charge le sous-titrage par le biais de fichiers WebVTT hébergés. Les légendes spécifiées avec ce paramètre s’appliquent à la vidéo qui vient en premier dans les visionneuses de supports ; les vidéos suivantes sont lues sans légende. Les signaux et les régions qui se chevauchent ne sont pas pris en charge. Opérateurs de positionnement des indices pris en charge :

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
   <td colname="col2"> <p>alignement de test </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> gauche|droite|milieu|début|fin  </span> </p> </td> 
   <td colname="col4"> <p> Contrôle l’alignement du texte. </p> <p>La valeur par défaut est <span class="codeph"> mid </span>. </p> </td> 
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
   <td colname="col4"> <p> Pourcentage de la largeur de vidéo utilisée pour les légendes. </p> <p>La valeur par défaut est <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>position de la ligne </p> </td> 
   <td colname="col3"> <p> 0 %-100 %|entier </p> </td> 
   <td colname="col4"> <p> Détermine la position de la ligne sur la page. </p> <p>S’il s’agit d’un entier sans signe de pourcentage, il s’agit du nombre de lignes du haut où le texte est affiché. </p> <p>Si elle est exprimée en pourcentage, le signe pourcentage est le dernier caractère, le texte de la légende s’affiche alors en pourcentage dans la zone d’affichage. </p> <p>La valeur par défaut est <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sachez que s’il existe d’autres fonctionnalités WebVTT présentes dans le fichier WebVTT, elles ne sont pas prises en charge ; cependant, ils ne perturberont pas le sous-titrage.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier  </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu de la légende WebVTT. Le fichier WebVTT est diffusé par Image Serving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Indique l’état de légende par défaut. </p> <p>Activé est <span class="codeph"> 1 </span>. </p> </td> 
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
