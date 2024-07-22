---
title: Mise en évidence de la cible
description: La mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 89f34a96-2b21-4169-8c25-4b53005e59b8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Mise en évidence de la cible{#focus-highlight}

La mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS**

L’aspect est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7interactiveimage *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> composition </span> </p> </td> 
   <td colname="col2"> <p>Style de mise en surbrillance du focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du focus du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7interactiveimage *:focus { 
 outline: none; 
}
```
