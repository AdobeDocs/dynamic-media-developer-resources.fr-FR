---
title: Mise au point
description: La mise en surbrillance de la mise au point d’entrée affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée par le sélecteur de classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f9343055-9fd9-4b19-bba3-1f742acb6193
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 1%

---

# Mise au point{#focus-highlight}

La mise en surbrillance de la mise au point d’entrée affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée par le sélecteur de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS**

L’apparence est contrôlée par le sélecteur de classe CSS suivant :

```
.s7carouselviewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contour </span> </p> </td> 
   <td colname="col2"> <p>Style de mise au point de mise en évidence. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du focus du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7carouselviewer *:focus { 
 outline: none; 
}
```
