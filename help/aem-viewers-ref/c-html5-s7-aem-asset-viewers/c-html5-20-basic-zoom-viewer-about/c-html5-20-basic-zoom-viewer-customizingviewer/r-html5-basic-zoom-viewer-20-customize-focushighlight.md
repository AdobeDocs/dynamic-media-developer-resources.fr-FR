---
description: La mise en surbrillance de la cible d’action affichée autour de l’élément d’interface d’utilisation de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.
seo-description: La mise en surbrillance de la cible d’action affichée autour de l’élément d’interface d’utilisation de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.
seo-title: Mise en évidence
solution: Experience Manager
title: Mise en évidence
uuid: 1b552aec-837a-4df4-91dc-615ceead92b3
feature: Dynamic Media Classic, Visionneuses, SDK/API, Zoom
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# Mise en évidence de la mise au point{#focus-highlight}

La mise en surbrillance de la cible d’action affichée autour de l’élément d’interface d’utilisation de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect est contrôlé à l’aide du sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> outline  </span> </p> </td> 
   <td colname="col2"> <p>Mise en surbrillance du focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour désactiver la mise en surbrillance par défaut du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7basiczoomviewer *:focus { 
 outline: none; 
}
```

