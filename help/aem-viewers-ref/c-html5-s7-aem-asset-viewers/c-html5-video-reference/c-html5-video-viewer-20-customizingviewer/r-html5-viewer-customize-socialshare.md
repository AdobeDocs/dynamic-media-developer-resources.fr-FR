---
description: L’outil de partage sur les réseaux sociaux s’affiche par défaut dans le coin supérieur droit. Il se compose d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et qui contient des outils de partage individuels.
seo-description: L’outil de partage sur les réseaux sociaux s’affiche par défaut dans le coin supérieur droit. Il se compose d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et qui contient des outils de partage individuels.
seo-title: Partage sur les réseaux sociaux
solution: Experience Manager
title: Partage sur les réseaux sociaux
topic: Dynamic media
uuid: 5c1ce7b4-54bf-486f-8b57-1d6d0cec119e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Partage sur les réseaux sociaux{#social-share}

L’outil de partage sur les réseaux sociaux s’affiche par défaut dans le coin supérieur droit. Il se compose d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et qui contient des outils de partage individuels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La position et la taille de l’outil de partage sur les réseaux sociaux dans l’interface utilisateur du lecteur de contenu sont contrôlées par les éléments suivants :

```
.s7videoviewer .s7socialshare
```

**Propriétés CSS de l’outil de partage sur les réseaux sociaux**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p> Position verticale de l’outil de partage sur les réseaux sociaux par rapport au  du lecteur de contenu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale de l’outil de partage sur les réseaux sociaux par rapport au  du lecteur de contenu. </p> </td> 
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

Exemple : configurez un outil de partage sur les réseaux sociaux positionné à quatre pixels du haut et à cinq pixels de la droite du du lecteur et dimensionné à 28 x 28 pixels.

```
.s7videoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

L’aspect du bouton de l’outil de partage sur les réseaux sociaux est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7socialshare .s7socialbutton
```

**Propriétés CSS du bouton social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
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

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple : configurez un bouton d’outil de partage sur les réseaux sociaux qui affiche une image différente pour chacun des quatre états de bouton.

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

L’aspect du panneau qui contient les icônes de partage sur les réseaux sociaux individuels est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7socialshare .s7socialsharepanel
```

**Propriétés CSS du panneau de partage sur les réseaux sociaux**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez un panneau pour obtenir une couleur transparente :

```
.s7videoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

