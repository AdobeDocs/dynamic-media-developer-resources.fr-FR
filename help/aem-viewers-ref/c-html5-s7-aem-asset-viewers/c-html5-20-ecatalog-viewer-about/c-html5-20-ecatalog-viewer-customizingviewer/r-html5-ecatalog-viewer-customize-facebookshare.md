---
title: Partager sur Facebook
description: L’outil de partage Facebook se compose d’un bouton ajouté au panneau Partage sur les réseaux sociaux . Lorsque le bouton est sélectionné, l’utilisateur est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil de partage sur les réseaux sociaux.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 0525bfd0-ce38-4fd1-a5cc-e6b5acab1651
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Partager sur Facebook{#facebook-share}

L’outil de partage Facebook se compose d’un bouton ajouté au panneau Partage sur les réseaux sociaux . Lorsque le bouton est sélectionné, l’utilisateur est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil de partage sur les réseaux sociaux.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L’aspect du bouton de partage Facebook est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7facebookshare
```

**Propriétés CSS de l’outil de partage Facebook**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau Partage sur les réseaux sociaux en définissant `display:none` propriété CSS sur sa classe CSS.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un bouton de partage Facebook de 28 x 28 pixels qui affiche une image différente pour chacun des quatre états de bouton différents :

```
.s7ecatalogviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
