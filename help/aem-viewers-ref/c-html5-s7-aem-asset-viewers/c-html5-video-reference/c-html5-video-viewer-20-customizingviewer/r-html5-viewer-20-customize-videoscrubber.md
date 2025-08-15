---
title: Curseur de progression vidéo
description: Le curseur vidéo est le curseur de contrôle horizontal qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# Curseur de progression vidéo{#video-scrubber}

Le curseur vidéo est le curseur horizontal qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Le « bouton » du curseur se déplace également pendant la lecture de la vidéo pour indiquer la position temporelle actuelle de la vidéo pendant la lecture. Le curseur de progression vidéo occupe toujours toute la largeur de la barre de contrôle. Il est possible d’habiller le laveur vidéo et de changer sa hauteur et sa position verticale, par CSS.

L’aspect général du curseur vidéo est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**Propriétés CSS du curseur de progression vidéo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris le rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure inférieure, remplissage compris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du laveur vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur du laveur vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les sélecteurs de classes CSS suivants suivent les indicateurs d’arrière-plan, de lecture et de chargement :

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**Propriétés CSS de la piste**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la piste correspondante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur de la piste correspondante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle le bouton :

```
.s7videoviewer .s7videoscrubber .s7knob
```

**Propriétés CSS du bouton**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p>Décalage vertical du bouton. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>Illustration de bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle la bulle de durée de lecture :

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**Propriétés CSS de la bulle de temps de lecture**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p> Famille de polices à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de taille de police </span> </p> </td> 
   <td colname="col2"> <p> Taille de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la zone des bulles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la zone des bulles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Remplissage de zone bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Illustration Bubble. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement de texte </span> </p> </td> 
   <td colname="col2"> <p>Alignement du texte sur la zone des bulles. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle de défilement vidéo peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

**Exemple** - Pour configurer une visionneuse de vidéos avec un curseur vidéo avec des couleurs de piste personnalisées. La barre de défilement doit avoir une hauteur de dix pixels et être positionnée à dix pixels et 35 pixels des bords supérieur et gauche de la barre de commande.

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Lorsque le chapitre vidéo est activé avec le paramètre `navigation`, les emplacements des chapitres s’affichent sous forme de marqueurs au-dessus de la piste de nettoyage vidéo.

Le marqueur de chapitre vidéo est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**Propriétés CSS du marqueur de chapitre vidéo**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du marqueur de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du marqueur de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Illustration du marqueur de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , que vous pouvez utiliser pour appliquer différents habillages à différents états de bouton. En particulier, correspond `selected='default'` à l’état par défaut du marqueur de chapitre vidéo et `selected='over'` est utilisé lorsque le marqueur de chapitre vidéo est activé par un mouvement de survol de souris ou tactile.

**Exemple** - Pour configurer un marqueur de chapitre vidéo de 5 x 8 pixels et utilise des illustrations différentes pour les états « Par défaut » et « Supérieur ».

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

La bulle de chapitre vidéo est positionnée au-dessus du marqueur de chapitre vidéo et affiche le titre, l’heure de début et la description d’un chapitre donné. Il est possible de contrôler la largeur maximale de bulle et le décalage vertical par rapport à la piste de lavage vidéo. Le reste est calculé automatiquement par le composant.

La bulle de chapitres vidéo est contrôlée par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**Propriétés CSS de la bulle de chapitres vidéo**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur max. </span> </p> </td> 
   <td colname="col2"> <p>Largeur maximale de la bulle de chapitres vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p>Décalage vertical par rapport à la piste de défilement vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer une bulle de chapitres vidéo de 235 pixels de large et de huit pixels à partir du bas de la piste de défilement vidéo.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

La bulle de chapitres vidéo se compose d’un en-tête et de contenu facultatifs. L’en-tête contient l’heure de début et le titre du chapitre facultatifs.

L’en-tête est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**Propriétés CSS de l’en-tête bulle de chapitre vidéo**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’en-tête à bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Remplissage intérieur du texte d’en-tête à bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de l’en-tête à bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur de ligne </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la ligne de texte de l’en-tête de bulle du chapitre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer un en-tête de bulle de chapitre vidéo d’une hauteur de 22 pixels, une hauteur de ligne de 22 pixels, une marge horizontale de 12 pixels et un arrière-plan gris.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

L’heure de début du chapitre vidéo est contrôlée par le sélecteur de classe CSS suivant :

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**Propriétés CSS de l’heure de début du chapitre vidéo**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Graisse de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Remplissage droit </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre l’heure de début et le titre du chapitre. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer l’heure de début du chapitre en utilisant la police Verdana grise de dix pixels et a un remplissage de dix pixels à droite.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

Le titre du chapitre vidéo est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**Propriétés CSS du titre du chapitre vidéo**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> d’épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Épaisseur de la police du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Titre du chapitre vidéo Famille de polices. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer un titre de chapitre vidéo qui utilise une police Verdana blanche et gras de dix pixels.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

La description du chapitre vidéo est contrôlée par le sélecteur de classe CSS suivant :

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**Propriétés CSS de la description du chapitre vidéo**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p>Description du chapitre vidéo couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Description du chapitre vidéo, couleur d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Description du chapitre vidéo Graisse de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Description du chapitre vidéo Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Description du chapitre vidéo Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur de ligne </span> </p> </td> 
   <td colname="col2"> <p>Description du chapitre vidéo : hauteur de ligne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Description du chapitre vidéo rembourrage intérieur. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer la description du chapitre vidéo à l’aide d’une police Verdana gris foncé de 11 pixels, avec un arrière-plan gris clair. Enfin, utilise une hauteur de ligne de cinq pixels, un remplissage horizontal de 12 pixels, un remplissage supérieur de 12 pixels et un remplissage inférieur de neuf pixels.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

Le connecteur de coin dans le bas de la bulle de chapitre est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**Propriétés CSS du connecteur wedge**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur de bordure </span> </p> </td> 
   <td colname="col2"> <p>Couleur du connecteur en coin. </p> <p>Défini comme <span class="codeph"> &lt;color&gt; transparent </span> de sorte que seule la couleur de la bordure supérieure soit définie et que les bordures restantes restent transparentes.&lt;/color&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur-bordure </span> </p> </td> 
   <td colname="col2"> <p> Largeur du connecteur en coin. </p> <p>Définie comme <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> de sorte que la même largeur soit définie uniquement pour les bordures horizontale et supérieure et que la largeur de la bordure inférieure soit <span class="codeph"> 0</span>&lt;/width&gt;&lt;/width&gt;. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p> Définit uniquement une marge inférieure négative. Elle doit avoir la même valeur que <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** – Pour configurer un connecteur en coin gris de six pixels :

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
