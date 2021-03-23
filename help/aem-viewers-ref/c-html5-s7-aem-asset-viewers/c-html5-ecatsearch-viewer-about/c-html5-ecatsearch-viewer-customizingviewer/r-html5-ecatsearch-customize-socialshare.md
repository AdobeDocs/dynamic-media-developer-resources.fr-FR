---
description: Par défaut, l’outil de partage sur les réseaux sociaux s’affiche dans le coin supérieur gauche. Il s’agit d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et qui contient des outils de partage individuels.
seo-description: Par défaut, l’outil de partage sur les réseaux sociaux s’affiche dans le coin supérieur gauche. Il s’agit d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et qui contient des outils de partage individuels.
seo-title: Partage sur les réseaux sociaux
solution: Experience Manager
title: Partage sur les réseaux sociaux
uuid: 6d463eb1-c6bf-4f1c-90e4-b5ef1e5a1538
feature: Dynamic Media Classic, Visionneuses, SDK/API, Recherche de catalogue électronique
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---


# Partage sur les réseaux sociaux{#social-share}

Par défaut, l’outil de partage sur les réseaux sociaux s’affiche dans le coin supérieur gauche. Il s’agit d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et qui contient des outils de partage individuels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La position et la taille de l’outil de partage sur les réseaux sociaux dans l’interface utilisateur du lecteur de contenu sont contrôlées par les éléments suivants :

```
.s7ecatalogsearchviewer .s7socialshare
```

**Propriétés CSS de l’outil de partage sur les réseaux sociaux**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Décalage par rapport au haut de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left  </span> </p> </td> 
   <td colname="col2"> <p> Distance du bouton suivant à gauche ou du côté gauche de la barre de contrôle s’il s’agit du premier bouton d’une rangée. </p> </td> 
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

Exemple : configurez un outil de partage sur les réseaux sociaux positionné à quatre pixels du haut et à cinq pixels de la droite du conteneur du lecteur et dimensionné à 28 x 28 pixels.

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

L’aspect du bouton d’outil de partage sur les réseaux sociaux est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**Propriétés CSS du bouton social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : configurez un bouton d’outil de partage sur les réseaux sociaux qui affiche une image différente pour chacun des quatre états de bouton différents.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

L’aspect du panneau qui contient les icônes de partage sur les réseaux sociaux est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
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

Exemple : configurez un panneau pour obtenir une couleur transparente :

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

