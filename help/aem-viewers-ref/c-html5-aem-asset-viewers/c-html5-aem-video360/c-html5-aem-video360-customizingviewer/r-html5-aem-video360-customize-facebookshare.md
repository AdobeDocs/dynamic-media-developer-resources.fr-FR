---
description: L’outil de partage Facebook est constitué d’un bouton ajouté au panneau de partage Social. Lorsque l’utilisateur clique sur le bouton, il est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil de partage Social.
solution: Experience Manager
title: Partage Facebook
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: 343cde8b-796a-420f-abb7-268b3791a684
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Partage Facebook{#facebook-share}

L’outil de partage Facebook est constitué d’un bouton ajouté au panneau de partage Social. Lorsque l’utilisateur clique sur le bouton, il est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil de partage Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L’aspect du bouton de partage Facebook est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7facebookshare
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
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau de partage Social en définissant la propriété `display:none` CSS sur sa classe CSS.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Exemple**  : pour configurer un bouton de partage Facebook de 28 x 28 pixels et afficher une image différente pour chacun des quatre états de bouton différents :

```
.s7video360viewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7video360viewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7video360viewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7video360viewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
