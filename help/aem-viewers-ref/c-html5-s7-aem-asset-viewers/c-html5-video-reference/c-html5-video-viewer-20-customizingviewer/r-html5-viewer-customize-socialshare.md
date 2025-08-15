---
title: Social partager
description: L’outil Partage sur les réseaux sociaux s’affiche par défaut dans le coin supérieur droit. Il se compose d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et contient des outils de partage individuels.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 82b482f9-b117-4529-a422-cdb0eead0031
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# Social partager{#social-share}

L’outil Partage sur les réseaux sociaux s’affiche par défaut dans le coin supérieur droit. Il se compose d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et contient des outils de partage individuels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La position et la taille de l’outil de partage sur les réseaux sociaux dans l’interface utilisateur de la visionneuse sont contrôlées par les éléments suivants :

```
.s7videoviewer .s7socialshare
```

**Propriétés CSS de l’outil de partage sur les réseaux sociaux**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p> Position verticale de l’outil de partage sur les réseaux sociaux par rapport au conteneur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Gauche </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale de l’outil de partage sur les réseaux sociaux par rapport au conteneur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’outil de partage sur les réseaux sociaux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’outil de partage social. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez un outil de partage social positionné à quatre pixels du haut et à cinq pixels de la droite du conteneur de la visionneuse et dont la taille est de 28 x 28 pixels.

```
.s7videoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

L’aspect du bouton de l’outil Partage sur les réseaux sociaux est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7socialshare .s7socialbutton
```

**Propriétés CSS du bouton social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état donné du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple - configurez un bouton d’outil de partage social qui affiche une image différente pour chacun des quatre états de bouton différents.

```
.s7videoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

L’apparence du panneau qui contient les différentes icônes de partage sur les réseaux sociaux est contrôlée par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7socialshare .s7socialsharepanel
```

**Propriétés CSS du panneau Partage social**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - configuration d’un panneau pour avoir une couleur transparente :

```
.s7videoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
