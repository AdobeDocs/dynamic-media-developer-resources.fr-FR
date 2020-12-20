---
description: Mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée.
seo-description: Mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée.
seo-title: Mise en évidence
solution: Experience Manager
title: Mise en évidence
topic: Dynamic media
uuid: 0bd36795-e663-4f0e-8310-a57c2ffae4a2
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# Mise en évidence de la mise au point{#focus-highlight}

Mise en surbrillance de la cible d’action affichée autour de l’élément d’interface utilisateur de la visionneuse ciblée.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

L’aspect de la mise en surbrillance de la cible d’action est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer *:focus
```

**Propriétés CSS de mise en surbrillance de la mise en surbrillance**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> outline  </span> </p> </td> 
   <td colname="col2"> <p> Mise en surbrillance du focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

