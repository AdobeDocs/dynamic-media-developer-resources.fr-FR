---
title: Mise en évidence de la cible
description: Mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse sélectionnée.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# Mise en évidence de la cible{#focus-highlight}

Mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse sélectionnée.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

L’aspect de la mise en surbrillance de la mise au point est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogviewer *:focus
```

**Propriétés CSS de mise en surbrillance de la mise au point**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> composition </span> </p> </td> 
   <td colname="col2"> <p> Style de mise en surbrillance du focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du focus du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
