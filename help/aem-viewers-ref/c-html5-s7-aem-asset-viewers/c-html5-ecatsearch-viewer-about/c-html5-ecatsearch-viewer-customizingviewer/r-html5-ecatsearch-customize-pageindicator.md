---
description: L’indicateur de page affiche l’index de la page active et le nombre total de pages. Il apparaît dans la barre de contrôle principale sur les ordinateurs de bureau et les tablettes, et sur les téléphones portables, il est ajouté à la barre de contrôle secondaire. L’indicateur de page peut être dimensionné, habillé et positionné par CSS.
seo-description: L’indicateur de page affiche l’index de la page active et le nombre total de pages. Il apparaît dans la barre de contrôle principale sur les ordinateurs de bureau et les tablettes, et sur les téléphones portables, il est ajouté à la barre de contrôle secondaire. L’indicateur de page peut être dimensionné, habillé et positionné par CSS.
seo-title: Indicateur de page
solution: Experience Manager
title: Indicateur de page
topic: Dynamic media
uuid: 1be6021b-3026-48ef-b121-eeb8270d2bae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Indicateur de page{#page-indicator}

L’indicateur de page affiche l’index de la page active et le nombre total de pages. Il apparaît dans la barre de contrôle principale sur les ordinateurs de bureau et les tablettes, et sur les téléphones portables, il est ajouté à la barre de contrôle secondaire. L’indicateur de page peut être dimensionné, habillé et positionné par CSS.

L’indicateur de page d’aspect est contrôlé à l’aide du sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite de la barre de contrôle principale (sur les ordinateurs de bureau et tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’indicateur de page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’indicateur de page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Police - Couleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un indicateur de page de 56 x 28 pixels, centré horizontalement et positionné à 4 pixels du bas de la barre de contrôle principale, utilisez une police Helvetica de 14 pixels.

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

