---
description: La mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.
solution: Experience Manager
title: Mise en évidence
feature: Dynamic Media Classic, Visionneuses, SDK/API, Zoom
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 1%

---


# Mise en évidence de la mise au point{#focus-highlight}

La mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS**

L’aspect est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7zoomviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> outline  </span> </p> </td> 
   <td colname="col2"> <p>Mise en surbrillance du focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7zoomviewer *:focus { 
 outline: none; 
}
```

