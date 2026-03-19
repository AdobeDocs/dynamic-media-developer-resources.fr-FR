---
title: bouton plein écran
description: Le bouton Plein écran fait en sorte que le lecteur vidéo de recadrage intelligent passe en mode Plein écran ou le quitte lorsqu’un utilisateur ou une utilisatrice clique dessus.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 79b57f6d-17d2-48af-9414-b0ab9d24fbdc
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# bouton plein écran{#full-screen-button}

Le bouton Plein écran fait en sorte que le lecteur vidéo de recadrage intelligent passe en mode Plein écran ou le quitte lorsqu’un utilisateur ou une utilisatrice clique dessus.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Vous pouvez dimensionner, appliquer une enveloppe et positionner le bouton plein écran, par rapport à la barre de contrôle qui le contient, par CSS.

L’aspect du bouton Plein écran est contrôlé par le sélecteur de classe CSS :

```
.s7smartcropvideoviewer .s7fullscreenbutton
```

**Propriétés CSS du bouton Plein écran**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure droite, marge intérieure incluse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure gauche, marge intérieure incluse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inférieur </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du bouton Plein écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton Plein écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les sélecteurs d&#39;attributs `state` et `selected`, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. En particulier, `selected='true'` correspond à l&#39;état « plein écran » et `selected='false'` correspond à l&#39;état « normal ».

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) pour plus d’informations.

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Pour configurer un bouton plein écran de 32 x 32 pixels positionné à 6 pixels des bords supérieur et droit de la barre de contrôle. Affichez également une image différente pour chacun des quatre états de bouton différents, qu’ils soient sélectionnés ou non.

```
.s7smartcropvideoviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
