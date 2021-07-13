---
description: La zone de vue principale est la zone occupée par la vue sur la fenêtre déroulante et les échantillons.
solution: Experience Manager
title: Zone de visionneuse principale
feature: Dynamic Media Classic,Visionneuses,SDK/API,Fenêtre déroulante
role: Developer,User
exl-id: bf928c22-23e9-4df3-b2d7-0841c64baf19
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# Zone de visionneuse principale{#main-viewer-area}

La zone de vue principale est la zone occupée par la vue sur la fenêtre déroulante et les échantillons.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7flyoutviewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une visionneuse de fenêtre déroulante avec un arrière-plan blanc ( `#FFFFFF`) et lui donner une taille de 260 x 500 pixels.

```
.s7flyoutviewer { 
 background-color: #FFFFFF; 
 width: 260px; 
 height: 500px;  
}
```
