---
description: La vue principale se compose de l’image agrandie.
solution: Experience Manager
title: Mode Zoom
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom
role: Developer,User
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 3%

---

# Mode Zoom{#zoom-view}

La vue principale se compose de l’image agrandie.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Le curseur s’affiche au-dessus de la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre la vue principale transparente.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sur les systèmes de bureau, le composant prend en charge le sélecteur d’attributs `cursortype` qui peut être appliqué à la classe `.s7zoomview` et contrôle le type de curseur en fonction de l’état du composant et de l’action de l’utilisateur. Les valeurs `cursortype` suivantes sont prises en charge :

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valeur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> par défaut </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image n’est pas agrandie en raison d’une petite résolution d’image, de paramètres de composant ou des deux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin  </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image peut être agrandie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> réinitialiser </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image atteint le niveau de zoom maximal et peut être réinitialisée à son état initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>Affiché lorsqu’un utilisateur effectue un panoramique sur l’image agrandie. </p> </td> 
  </tr> 
 </tbody> 
</table>
