---
title: Barre de contrôle secondaire
description: La barre de contrôle secondaire est la zone rectangulaire qui contient les boutons Première et Dernière page et un indicateur de page lorsqu’elle est disponible dans CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Barre de contrôle secondaire{#secondary-control-bar}

La barre de contrôle secondaire est la zone rectangulaire qui contient les boutons Première et Dernière page et un indicateur de page lorsqu’elle est disponible dans CSS.

Par défaut, il s’affiche uniquement sur les téléphones mobiles, dans la partie inférieure de la visionneuse. Prend toujours toute la largeur disponible de la visionneuse. Il est possible de modifier sa couleur, sa hauteur et sa position verticale par CSS, par rapport au conteneur de la visionneuse.

L’apparence de la barre de contrôle secondaire est contrôlée par le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p>Position depuis le haut de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p>Position depuis le bas de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle secondaire. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une barre de contrôle secondaire grise de 72 pixels de haut et placée au bas du conteneur de la visionneuse.

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
