---
description: La vue principale est constituée de l’image à 360° lorsque l’élément actif est une visionneuse à 360°.
solution: Experience Manager
title: Vue à 360°
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---


# Vue à 360°{#spin-view}

La vue principale est constituée de l’image à 360° lorsque l’élément actif est une visionneuse à 360°.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visualisation principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal de la vue de rotation. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour rendre la vue de rotation transparente.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

