---
description: Par défaut, l’outil de partage sur les réseaux sociaux s’affiche dans le coin supérieur droit. Il s’agit d’un bouton et d’un panneau qui se développent lorsque l’utilisateur clique ou appuie sur un bouton et qui contient des outils de partage individuels.
solution: Experience Manager
title: Partage sur les réseaux sociaux
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: 4bc951ae-2b9a-4cbe-9288-170c576b3b7b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 1%

---

# Partage sur les réseaux sociaux{#social-share}

Par défaut, l’outil de partage sur les réseaux sociaux s’affiche dans le coin supérieur droit. Il s’agit d’un bouton et d’un panneau qui se développent lorsque l’utilisateur clique ou appuie sur un bouton et qui contient des outils de partage individuels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La position et la taille de l’outil de partage sur les réseaux sociaux dans l’interface utilisateur du lecteur de contenu sont contrôlées par les éléments suivants :

```
.s7video360viewer .s7socialshare
```

**Propriétés CSS de l’outil de partage sur les réseaux sociaux**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p> Position verticale de l’outil de partage sur les réseaux sociaux par rapport au conteneur du lecteur de contenu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale de l’outil de partage sur les réseaux sociaux par rapport au conteneur du lecteur de contenu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’outil de partage sur les réseaux sociaux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’outil de partage sur les réseaux sociaux. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**  : pour configurer un outil de partage sur les réseaux sociaux positionné à quatre pixels du haut et à cinq pixels de la droite du conteneur de la visionneuse et de 28 x 28 pixels.

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

L’aspect du bouton d’outil de partage sur les réseaux sociaux est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7socialshare .s7socialbutton
```

**Propriétés CSS du bouton d’outil de partage sur les réseaux sociaux**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
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

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Exemple**  : pour configurer un bouton d’outil de partage sur les réseaux sociaux qui affiche une image différente pour chacun des quatre états de bouton différents.

```
.s7video360viewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

L’aspect du panneau qui contient les icônes de partage sur les réseaux sociaux est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7socialshare .s7socialsharepanel
```

**Propriétés CSS du panneau de partage sur les réseaux sociaux**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**  - Pour configurer un panneau de couleur transparente :

```
.s7video360viewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
