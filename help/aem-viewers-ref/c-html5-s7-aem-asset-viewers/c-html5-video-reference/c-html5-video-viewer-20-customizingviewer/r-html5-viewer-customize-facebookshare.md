---
description: L’outil de partage Facebook est constitué d’un bouton ajouté au panneau de partage Social. Lorsque l’utilisateur clique sur le bouton, il est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil de partage Social.
seo-description: L’outil de partage Facebook est constitué d’un bouton ajouté au panneau de partage Social. Lorsque l’utilisateur clique sur le bouton, il est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil de partage Social.
seo-title: Partage Facebook
solution: Experience Manager
title: Partage Facebook
topic: Dynamic media
uuid: 0327631d-9847-409c-bce1-e58ee248d701
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Partage Facebook{#facebook-share}

L’outil de partage Facebook est constitué d’un bouton ajouté au panneau de partage Social. Lorsque l’utilisateur clique sur le bouton, il est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil de partage Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L’aspect du bouton de partage Facebook est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7facebookshare
```

**Propriétés CSS de l’outil de partage Facebook**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’ `state` attributs, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau de partage Social en définissant la propriété `display:none` CSS sur sa classe CSS.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple : pour configurer un bouton de partage Facebook de 28 x 28 pixels et afficher une image différente pour chacun des quatre états de bouton différents :

```
.s7videoviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7videoviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7videoviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7videoviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```

