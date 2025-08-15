---
title: barre de contrôle Secondaire
description: La barre de contrôle secondaire est la zone rectangulaire qui contient les boutons Première et Dernière page et un indicateur de page lorsqu’il est disponible dans CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 2354c3a0-2df7-4a18-aac1-fac158a9b659
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# barre de contrôle Secondaire{#secondary-control-bar}

La barre de contrôle secondaire est la zone rectangulaire qui contient les boutons Première et Dernière page et un indicateur de page lorsqu’il est disponible dans CSS.

Par défaut, il s’affiche uniquement sur les téléphones mobiles et est positionné dans la partie inférieure de la visionneuse. Elle utilise toujours la largeur totale de visionneuse disponible. Il est possible de modifier sa couleur, sa hauteur et sa position verticale par CSS, par rapport au conteneur de la visionneuse.

L’aspect de la barre de contrôle secondaire est contrôlé avec le sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du haut de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inférieur </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du bas de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d'arrière-plan de la barre de contrôle secondaire. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une barre de contrôle secondaire grise de 72 pixels de haut placée au bas du conteneur de la visionneuse.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
