---
title: Effet d’icône
description: L’indicateur de zoom est superposé sur la zone d’affichage principale. Il s’affiche lorsque l’image est dans un état réinitialisé et dépend également du paramètre iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 90877e39-04ac-4c6c-b7c9-98ffda9355f2
TQID: 'https://experienceleague.adobe.com/qXz02dVCo6RrhyN3OBX4wklmho8pyFUQ0HdcgCPjD-k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 0%

---

# Effet d’icône{#icon-effect}

L’indicateur de zoom est superposé sur la zone d’affichage principale. Il s’affiche lorsque l’image est dans un état réinitialisé et dépend également du paramètre iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7pageview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Illustration de l’indicateur de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’indicateur de zoom en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’indicateur de zoom en pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’effet Icône prend en charge le sélecteur d’attributs `media-type`, que vous pouvez utiliser pour appliquer différents effets d’icône sur différents appareils. En particulier, `media-type='standard'` correspond à des systèmes de bureau où l&#39;entrée souris est normalement utilisée et `media-type='multitouch'` correspond à des appareils à entrée tactile.

Exemple : pour configurer un indicateur de zoom de 100 x 100 pixels avec différentes illustrations pour les ordinateurs de bureau et les appareils tactiles.

```
.s7ecatalogsearchviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogsearchviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogsearchviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
