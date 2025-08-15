---
title: Mise au point
description: La mise en surbrillance de la mise au point d’entrée affichée autour de l’élément d’interface d’utilisation de la visionneuse ciblée est contrôlée par le sélecteur de classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 74ff9669-d56b-4731-9d4a-dda7c831e162
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Mise au point{#focus-highlight}

La mise en surbrillance de la mise au point d’entrée affichée autour de l’élément d’interface d’utilisation de la visionneuse ciblée est contrôlée par le sélecteur de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’apparence est contrôlée par le sélecteur de classe CSS suivant :

```
.s7basiczoomviewer *:focus
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
.s7basiczoomviewer *:focus { 
 outline: none; 
}
```
