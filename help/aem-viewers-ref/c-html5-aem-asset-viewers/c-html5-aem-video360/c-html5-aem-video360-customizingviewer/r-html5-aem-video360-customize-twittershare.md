---
title: Partage Twitter
description: L’outil de partage Twitter consiste en un bouton ajouté au panneau de partage Social. Lorsque le bouton est sélectionné, l’utilisateur est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil de partage Social.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a90a4c82-b51a-4fb0-9196-44ae4ba8e0cd
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Partage Twitter{#twitter-share}

L’outil de partage Twitter consiste en un bouton ajouté au panneau de partage Social. Lorsque le bouton est sélectionné, l’utilisateur est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil de partage Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L’aspect du bouton de partage Twitter est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7twittershare
```

**Propriétés CSS de l’outil de partage Twitter**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état donné du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau de partage Social en définissant `display:none` la propriété CSS sur sa classe CSS.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) de l’interface utilisateur.

**Exemple** : pour configurer un bouton de partage Twitter de 28 x 28 pixels qui affiche une image différente pour chacun des quatre états différents du bouton :

```
.s7video360viewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7video360viewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7video360viewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7video360viewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
