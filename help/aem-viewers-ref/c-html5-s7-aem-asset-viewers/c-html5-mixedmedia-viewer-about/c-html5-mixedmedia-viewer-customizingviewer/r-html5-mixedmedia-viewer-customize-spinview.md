---
description: Le principal est constitué de l’image à 360° lorsque le fichier actif est une visionneuse à 360°.
seo-description: Le principal est constitué de l’image à 360° lorsque le fichier actif est une visionneuse à 360°.
seo-title: à 360°
solution: Experience Manager
title: à 360°
topic: Dynamic media
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Spin view{#spin-view}

Le principal est constitué de l’image à 360° lorsque le fichier actif est une visionneuse à 360°.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal du à 360°. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre le à 360° transparent.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

