---
title: Indicateur de page
description: L’indicateur de page affiche l’index de la page actuelle et le nombre total de pages. Il apparaît dans la barre de contrôle principale sur les systèmes de bureau et les tablettes, sur les téléphones mobiles, il est ajouté à la barre de contrôle secondaire. L’indicateur de page peut être dimensionné, habillé et positionné par CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Indicateur de page{#page-indicator}

L’indicateur de page affiche l’index de la page actuelle et le nombre total de pages. Il apparaît dans la barre de contrôle principale sur les systèmes de bureau et les tablettes, sur les téléphones mobiles, il est ajouté à la barre de contrôle secondaire. L’indicateur de page peut être dimensionné, habillé et positionné par CSS.

L’indicateur de page d’apparence est contrôlé par le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’indicateur de page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’indicateur de page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un indicateur de page de 56 x 28 pixels, centré horizontalement et positionné à 4 pixels du bas de la barre de contrôle principale, utilisez une police Helvetica® de 14 pixels.

```
.s7ecatalogsearchviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```
