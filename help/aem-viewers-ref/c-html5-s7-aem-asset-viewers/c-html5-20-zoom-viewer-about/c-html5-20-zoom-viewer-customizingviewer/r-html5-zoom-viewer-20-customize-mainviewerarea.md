---
title: Zone de visionneuse principale
description: La zone d’affichage principale est la zone occupée par l’image du zoom et les échantillons. Il est généralement configuré pour s’adapter à l’écran de l’appareil disponible lorsqu’aucune taille n’est spécifiée.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
TQID: 'https://experienceleague.adobe.com/mAfXI6eLoLmVR7yI6EvUjlVjQrQ8J86ikUZGa5rRN4E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 0%

---

# Zone de visionneuse principale{#main-viewer-area}

La zone d’affichage principale est la zone occupée par l’image du zoom et les échantillons. Il est généralement configuré pour s’adapter à l’écran de l’appareil disponible lorsqu’aucune taille n’est spécifiée.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Lorsque vous travaillez en mode incorporé (lorsqu’une taille explicite est donnée à la zone de visionneuse principale), la visionneuse réduit automatiquement la hauteur de sa zone principale de la hauteur du composant Nuancier qui travaille avec l’image unique. Par conséquent, les nuanciers ne sont pas nécessaires.

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7zoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une visionneuse sur fond blanc ( `#FFFFFF`) et définir sa taille sur 512 x 288 pixels.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

