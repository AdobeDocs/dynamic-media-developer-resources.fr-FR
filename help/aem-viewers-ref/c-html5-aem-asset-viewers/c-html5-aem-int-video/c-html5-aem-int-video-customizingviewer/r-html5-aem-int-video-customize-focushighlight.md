---
title: Mettre en surbrillance
description: La mise en surbrillance de la sélection d’entrée affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: cb5231ed-106a-444f-aac7-06dd1a84a665
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 1%

---

# Mettre en surbrillance{#focus-highlight}

La mise en surbrillance de la sélection d’entrée affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS**

L’aspect est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> de plan </span> </p> </td> 
   <td colname="col2"> <p>Style de surbrillance du focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```
