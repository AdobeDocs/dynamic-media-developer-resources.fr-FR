---
title: légende
description: Paramètre commun à tous les observateurs.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
TQID: 'https://experienceleague.adobe.com/ydZxVPE4iwQMlJLnmCFXeAzkVX2cSGiuDzeNeEi5iaU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 5%

---

# légende{#caption}

Paramètre commun à tous les observateurs.

>[!NOTE]
>
>Cette commande ne concerne pas la visionneuse d’images vidéo.

` caption= *`fichier`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu de légende WebVTT. La diffusion d’images diffuse le fichier WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Indique l’état de légende par défaut. Activé est <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Cette visionneuse prend en charge les légendes au moyen de fichiers WebVTT hébergés. Les sous-titres spécifiés avec ce paramètre s’appliquent à la vidéo qui apparaît en premier dans les visionneuses de médias ; les vidéos suivantes sont lues sans sous-titres. Les zones géographiques et les indices de chevauchement ne sont pas pris en charge. Opérateurs de positionnement des repères pris en charge :

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
   <td colname="col1"> <p> <span class="codeph"> UN </span> </p> </td> 
   <td colname="col2"> <p>test d'alignement </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> gauche|droite|milieu|début|fin </span> </p> </td> 
   <td colname="col4"> <p> Contrôle l’alignement du texte. </p> <p>La valeur par défaut est <span class="codeph"> moyenne </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>position du texte </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Pourcentage d’insertion dans le composant VideoPlayer au début du texte de la légende. </p> <p>La valeur par défaut est <span class="codeph"> 0 % </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>taille de la ligne </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Pourcentage de largeur vidéo utilisé pour les sous-titres. </p> <p>La valeur par défaut est <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>position de la ligne </p> </td> 
   <td colname="col3"> <p> 0%-100%|entier </p> </td> 
   <td colname="col4"> <p> Détermine la position de la ligne sur la page. </p> <p>S’il est exprimé sous la forme d’un entier sans signe de pourcentage, il s’agit du nombre de lignes à partir du haut où le texte est affiché. </p> <p>S’il est exprimé en pourcentage (le signe de pourcentage est le dernier caractère), le texte de la légende s’affiche en pourcentage dans la zone d’affichage. </p> <p>La valeur par défaut est <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Si d’autres fonctionnalités WebVTT sont présentes dans le fichier WebVTT, elles ne sont pas prises en charge. Toutefois, elles n’interrompent pas le sous-titrage.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu de légende WebVTT. Le fichier WebVTT est diffusé par le service d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
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
