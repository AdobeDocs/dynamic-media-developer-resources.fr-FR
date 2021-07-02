---
description: L’indicateur de zoom est superposé sur la zone d’affichage du zoom. Elle s’affiche lorsque l’image est à l’état réinitialisé et dépend également du paramètre iconEffet.
solution: Experience Manager
title: Effet de l’icône de vue Zoom
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: f2db0259-f1cf-41bc-86fd-97a40d01db16
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# Effet de l’icône de vue Zoom{#zoom-view-icon-effect}

L’indicateur de zoom est superposé sur la zone d’affichage du zoom. Elle s’affiche lorsque l’image est à l’état réinitialisé et dépend également du paramètre iconEffet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Illustration de l’indicateur de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’indicateur de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’indicateur de zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’effet Icône prend en charge le sélecteur d’attributs `media-type`, que vous pouvez utiliser pour appliquer différents effets d’icône sur différents appareils. En particulier, `media-type='standard'` correspond aux systèmes de bureau où l’entrée de la souris est normalement utilisée et `media-type='multitouch'` correspond aux appareils avec l’entrée tactile.

Exemple : pour configurer un indicateur de zoom de 100 x 100 pixels avec différentes illustrations pour les systèmes de bureau et les appareils tactiles.

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
