---
title: Partage social
description: Par défaut, l’outil Partage sur les réseaux sociaux s’affiche dans le coin supérieur gauche. Il se compose d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et contient des outils de partage individuels.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5cac6c86-08fb-46fd-bab0-ab77154eb770
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Partage social{#social-share}

Par défaut, l’outil Partage sur les réseaux sociaux s’affiche dans le coin supérieur gauche. Il se compose d’un bouton et d’un panneau qui se développe lorsque l’utilisateur clique ou appuie sur un bouton et contient des outils de partage individuels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La position et la taille de l’outil de partage sur les réseaux sociaux dans l’interface utilisateur de la visionneuse sont contrôlées par les éléments suivants :

```
.s7ecatalogsearchviewer .s7socialshare
```

**Propriétés CSS de l’outil de partage sur les réseaux sociaux**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de la marge supérieure </span> </p> </td> 
   <td colname="col2"> <p> Décalage par rapport au haut de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge=</span> gauche </p> </td> 
   <td colname="col2"> <p> Distance par rapport au bouton suivant à gauche, ou sur le côté gauche de la barre de contrôle si ce bouton est le premier d’une ligne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’outil de partage sur les réseaux sociaux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’outil de partage sur les réseaux sociaux. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - configurez un outil de partage sur les réseaux sociaux qui se situe à quatre pixels du haut et à cinq pixels de la droite du conteneur de la visionneuse et est dimensionné de manière à avoir une taille de 28 x 28 pixels.

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

L’aspect du bouton de l’outil de partage sur les réseaux sociaux est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**Propriétés CSS du bouton social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - Configurez un bouton d’outil de partage sur les réseaux sociaux qui affiche une image différente pour chacun des quatre états de bouton différents.

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

**Propriétés CSS du panneau Partage sur les réseaux sociaux**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Configurez un panneau pour qu’il ait une couleur transparente :

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
