---
description: La barre de contrôle secondaire est la zone rectangulaire qui contient les boutons Première page et Dernière page et un indicateur de page lorsqu’il est disponible en CSS.
seo-description: La barre de contrôle secondaire est la zone rectangulaire qui contient les boutons Première page et Dernière page et un indicateur de page lorsqu’il est disponible en CSS.
seo-title: Barre de contrôle Secondaire
solution: Experience Manager
title: Barre de contrôle Secondaire
topic: Dynamic Media
uuid: 9a91da6b-0d9b-4b4c-9659-86a64e624947
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---


# Barre de contrôle Secondaire{#secondary-control-bar}

La barre de contrôle secondaire est la zone rectangulaire qui contient les boutons Première page et Dernière page et un indicateur de page lorsqu’il est disponible en CSS.

Par défaut, elle s’affiche uniquement sur les téléphones mobiles et se trouve dans le bas du lecteur de contenu. Elle prend toujours la largeur de visionneuse disponible dans son intégralité. Il est possible de modifier sa couleur, sa hauteur et sa position verticale par CSS, par rapport au conteneur de la visionneuse.

L’aspect de la barre de contrôle secondaire est contrôlé par le sélecteur de classe CSS suivant :

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

Exemple : pour configurer une barre de contrôle secondaire grise de 72 pixels et positionnée au bas du conteneur de la visionneuse.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

