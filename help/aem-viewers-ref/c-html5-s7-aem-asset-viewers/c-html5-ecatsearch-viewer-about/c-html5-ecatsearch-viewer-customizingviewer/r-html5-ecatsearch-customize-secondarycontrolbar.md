---
description: La barre de contrôle secondaire est la zone rectangulaire qui contient les boutons Première et Dernière page et un Indicateur de page lorsqu’il est disponible dans CSS.
solution: Experience Manager
title: Barre de contrôle Secondaire
feature: Dynamic Media Classic,Visionneuses,SDK/API,Recherche catalogue électronique
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 2%

---

# Barre de contrôle Secondaire{#secondary-control-bar}

La barre de contrôle secondaire est la zone rectangulaire qui contient les boutons Première et Dernière page et un Indicateur de page lorsqu’il est disponible dans CSS.

Par défaut, elle s’affiche uniquement sur les téléphones mobiles et se trouve au bas de la visionneuse. Il prend toujours toute la largeur disponible de la visionneuse. Il est possible de modifier sa couleur, sa hauteur et sa position verticale par CSS, par rapport au conteneur de la visionneuse.

L’aspect de la barre de contrôle secondaire est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du haut de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du bas de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle secondaire. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une barre de contrôle secondaire grise de 72 pixels de haut et positionnée au bas du conteneur de la visionneuse.

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
