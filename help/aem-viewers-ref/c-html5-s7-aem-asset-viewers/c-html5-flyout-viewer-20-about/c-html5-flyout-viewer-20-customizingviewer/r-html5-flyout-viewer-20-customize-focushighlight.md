---
description: La mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.
solution: Experience Manager
title: Mise en évidence de la cible
feature: Dynamic Media Classic,Visionneuses,SDK/API,Fenêtre déroulante
role: Developer,User
exl-id: 2cb2e719-ee56-45e5-a509-7e13bb3c2165
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 1%

---

# Mise en évidence de la cible{#focus-highlight}

La mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS**

L’aspect est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7flyoutviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> composition  </span> </p> </td> 
   <td colname="col2"> <p>Style de mise en surbrillance du focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du focus du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7flyoutviewer *:focus { 
 outline: none; 
}
```
