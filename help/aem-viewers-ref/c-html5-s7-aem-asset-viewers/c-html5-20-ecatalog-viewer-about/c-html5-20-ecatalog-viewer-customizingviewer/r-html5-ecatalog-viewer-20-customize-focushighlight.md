---
title: Mise au point
description: Mise en surbrillance de l’axe d’entrée affichée autour de l’élément d’interface utilisateur de la visionneuse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# Mise au point{#focus-highlight}

Mise en surbrillance de l’axe d’entrée affichée autour de l’élément d’interface utilisateur de la visionneuse.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

L’aspect de la mise en surbrillance du focus est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer *:focus
```

**Propriétés CSS de la mise en surbrillance**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contour </span> </p> </td> 
   <td colname="col2"> <p> Style de mise au point de mise en évidence. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du focus du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
