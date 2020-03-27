---
description: Mise en surbrillance du focus d’entrée affichée autour de l’élément d’interface utilisateur du lecteur ciblé.
seo-description: Mise en surbrillance du focus d’entrée affichée autour de l’élément d’interface utilisateur du lecteur ciblé.
seo-title: Mise en valeur
solution: Experience Manager
title: Mise en valeur
topic: Dynamic media
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Mise en valeur{#focus-highlight}

Mise en surbrillance du focus d’entrée affichée autour de l’élément d’interface utilisateur du lecteur ciblé.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

L’aspect de la mise en surbrillance de focus est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer *:focus
```

**Propriétés CSS de mise en surbrillance active**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> outline </span> </p> </td> 
   <td colname="col2"> <p> Mise au point du style de mise en surbrillance. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

