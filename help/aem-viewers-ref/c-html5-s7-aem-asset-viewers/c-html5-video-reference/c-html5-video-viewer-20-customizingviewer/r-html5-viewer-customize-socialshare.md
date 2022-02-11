---
title: Partage sur les réseaux sociaux
description: Par défaut, l’outil de partage sur les réseaux sociaux s’affiche dans le coin supérieur droit. Il se compose d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et contient des outils de partage individuels.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 82b482f9-b117-4529-a422-cdb0eead0031
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 1%

---

# Partage sur les réseaux sociaux{#social-share}

Par défaut, l’outil de partage sur les réseaux sociaux s’affiche dans le coin supérieur droit. Il se compose d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et contient des outils de partage individuels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La position et la taille de l’outil de partage sur les réseaux sociaux dans l’interface utilisateur de la visionneuse sont contrôlées par les éléments suivants :

```
.s7videoviewer .s7socialshare
```

**Propriétés CSS de l’outil de partage sur les réseaux sociaux**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p> Position verticale de l’outil de partage sur les réseaux sociaux par rapport au conteneur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale de l’outil de partage sur les réseaux sociaux par rapport au conteneur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’outil de partage sur les réseaux sociaux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l'outil de partage sur les réseaux sociaux. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez un outil de partage sur les réseaux sociaux qui est positionné à quatre pixels du haut et à cinq pixels de la droite du conteneur de la visionneuse et qui est dimensionné à 28 x 28 pixels.

```
.s7videoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

L’aspect du bouton de l’outil de partage sur les réseaux sociaux est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7videoviewer .s7socialshare .s7socialbutton
```

**Propriétés CSS du bouton social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge `state` sélecteur d’attributs qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle de bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) pour plus d’informations.

Exemple : configurez un bouton de l’outil de partage sur les réseaux sociaux qui affiche une image différente pour chacun des quatre états de bouton différents.

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

L’aspect du panneau qui contient les icônes de partage sur les réseaux sociaux individuelles est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7videoviewer .s7socialshare .s7socialsharepanel
```

**Propriétés CSS du panneau de partage social**

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
