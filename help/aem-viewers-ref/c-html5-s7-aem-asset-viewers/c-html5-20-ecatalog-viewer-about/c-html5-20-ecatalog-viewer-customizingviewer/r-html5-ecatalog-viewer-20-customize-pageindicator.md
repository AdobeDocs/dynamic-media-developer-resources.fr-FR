---
title: Indicateur de page
description: L’indicateur Page affiche l’index de la page active et le nombre total de pages. Il apparaît dans la barre de contrôle principale des ordinateurs de bureau et des tablettes, et sur les téléphones mobiles, il est ajouté à la barre de contrôle secondaire. L’indicateur de page peut être dimensionné, peint et positionné par CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: c63af583-274c-4052-8186-604119a368af
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Indicateur de page{#page-indicator}

L’indicateur Page affiche l’index de la page active et le nombre total de pages. Il apparaît dans la barre de contrôle principale des ordinateurs de bureau et des tablettes, et sur les téléphones mobiles, il est ajouté à la barre de contrôle secondaire. L’indicateur de page peut être dimensionné, peint et positionné par CSS.

L’aspect de l’indicateur de page est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure de la barre de contrôle principale (sur les ordinateurs de bureau et tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite de la barre de contrôle principale (sur les ordinateurs de bureau et tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche de la barre de contrôle principale (sur les ordinateurs de bureau et tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure de la barre de contrôle principale (sur les ordinateurs de bureau et tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la marge intérieure. </p> </td> 
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
   <td colname="col2"> <p>Couleur de la police. </p> </td> 
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

Exemple : pour configurer un indicateur de page de 56 x 28 pixels, centré horizontalement et positionné 4 pixels au bas de la barre de contrôle principale, et utiliser une police Helvetica® de 14 pixels.

```
.s7ecatalogviewer  .s7pageindicator { 
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
