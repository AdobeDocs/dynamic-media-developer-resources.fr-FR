---
title: Zone principale de la visionneuse
description: La zone d’affichage principale est la zone occupée par l’image de rotation. En règle générale, elle est configurée pour s’adapter à l’écran disponible du périphérique lorsqu’aucune taille n’est spécifiée.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 6cd9c375-8890-4033-b187-b95b26dd6009
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Zone principale de la visionneuse{#main-viewer-area}

La zone d’affichage principale est la zone occupée par l’image de rotation. En règle générale, elle est configurée pour s’adapter à l’écran disponible du périphérique lorsqu’aucune taille n’est spécifiée.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone principale de la visionneuse**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7spinviewer
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
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur de fond au format hexadécimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer une visionneuse avec un fond blanc ( `#FFFFFF`) et faire sa taille 512 x 288 pixels.

```
.s7spinviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
