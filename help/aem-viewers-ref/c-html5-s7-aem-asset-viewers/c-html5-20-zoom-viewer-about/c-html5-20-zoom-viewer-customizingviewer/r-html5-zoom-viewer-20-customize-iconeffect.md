---
title: Effet Icône
description: L’indicateur de zoom est superposé sur la zone d’affichage principale. Elle s’affiche lorsque l’image est à l’état réinitialisé et dépend également du paramètre iconEffet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 5f50cb66-e5b4-42c6-8917-a954d8d80154
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---

# Effet Icône{#icon-effect}

L’indicateur de zoom est superposé sur la zone d’affichage principale. Elle s’affiche lorsque l’image est à l’état réinitialisé et dépend également du paramètre iconEffet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7zoomviewer .s7zoomview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Illustration de l’indicateur de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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
>L’effet d’icône prend en charge `media-type` sélecteur d’attributs que vous pouvez utiliser pour appliquer différents effets d’icône sur différents appareils. En particulier, `media-type='standard'` correspond aux systèmes de bureau où la saisie de la souris est normalement utilisée et `media-type='multitouch'` correspond aux périphériques avec une entrée tactile.

Exemple : pour configurer un indicateur de zoom de 100 x 100 pixels avec différentes illustrations pour les systèmes de bureau et les appareils tactiles.

```
.s7zoomviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7zoomviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7zoomviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
