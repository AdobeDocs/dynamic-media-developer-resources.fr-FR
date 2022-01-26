---
title: Vue à 360°
description: La vue principale est composée de l’image à 360° lorsque la ressource active est une visionneuse à 360°.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---

# Vue à 360°{#spin-view}

La vue principale est composée de l’image à 360° lorsque la ressource active est une visionneuse à 360°.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal de la vue à 360°. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre la vue à 360° transparente.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
