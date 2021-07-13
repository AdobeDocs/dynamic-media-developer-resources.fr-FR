---
description: La vue principale se compose de l’image statique.
solution: Experience Manager
title: Mode Zoom
feature: Dynamic Media Classic,Visionneuses,SDK/API,Images interactives
role: Developer,User
exl-id: e83d53a1-bee9-4e4d-8295-a3a350f3ff9c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---

# Mode Zoom{#zoom-view}

La vue principale se compose de l’image statique.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7interactiveimage .s7zoomview
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
 </tbody> 
</table>

Exemple : pour rendre la vue principale transparente.

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```
