---
title: Nettoyeur vidéo
description: La barre vidéo est la commande de curseur horizontal qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9d11f2e9-315c-44d8-beb1-530d2b316604
TQID: 'https://experienceleague.adobe.com/XLrCMFCLFFTSX4dvx84u0LeR-46CRfyzkTNQuWSlwk0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1063
ht-degree: 0%

---

# Nettoyeur vidéo{#video-scrubber}

La barre vidéo est la commande de curseur horizontal qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Le « bouton » de la barre de défilement se déplace également lors de la lecture de la vidéo pour indiquer la position temporelle actuelle de la vidéo pendant la lecture. La barre de défilement prend toujours toute la largeur de la barre de contrôle. Il est possible d’appliquer une peau à la barre vidéo et de modifier sa hauteur et sa position verticale, par CSS.

L’aspect général de la barre vidéo est contrôlé par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**Propriétés CSS de la barre vidéo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> inférieur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure inférieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur de la barre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les sélecteurs de classe CSS suivants effectuent le suivi des indicateurs d’arrière-plan, de lecture et de chargement :

```
.s7interactivevideoviewer .s7videoscrubber .s7track 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed
```

**Propriétés CSS de la piste**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la piste correspondante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur de la piste correspondante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle le bouton :

```
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**Propriétés CSS du bouton**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Décalage vertical du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Oeuvre d'art de bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle la bulle de durée de lecture :

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
```

**Propriétés CSS de la bulle de temps de lecture**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p> Famille de polices à utiliser pour le texte d’affichage de l’heure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Taille de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Couleur de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Illustration Bubble. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> d’alignement de texte </p> </td> 
   <td colname="col2"> <p>Alignement du texte sur la zone de bulle. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle de la barre vidéo peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

**Exemple** - Pour configurer une visionneuse de vidéos avec une barre vidéo et des couleurs de piste personnalisées qui font dix pixels de haut. Positionnez-le à dix pixels et 35 pixels des bords supérieur et gauche de la barre de contrôle.

```
.s7interactivevideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Lorsque le marqueur de chapitre vidéo est activé avec le paramètre `navigation`, les emplacements de chapitre s’affichent en tant que marqueurs au-dessus de la piste de nettoyage vidéo.

Le marqueur de chapitre vidéo est contrôlé par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

**Propriétés CSS du marqueur de chapitre vidéo**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du marqueur de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du marqueur de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Illustration du marqueur de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, que vous pouvez utiliser pour appliquer différents habillages à différents états de bouton. En particulier, `selected='default'` correspond à l’état par défaut du marqueur de chapitre vidéo et `selected='over'` est utilisé lorsque le marqueur de chapitre vidéo est activé par un geste de survol ou de toucher de la souris.

**Exemple** - Pour configurer un marqueur de chapitre vidéo de 5 x 8 pixels qui utilise des illustrations différentes pour les états « par défaut » et « dépassé ».

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

La bulle de chapitre vidéo est positionnée au-dessus du marqueur de chapitre vidéo et affiche le titre, l’heure de début et la description d’un chapitre donné. Il est possible de contrôler la largeur de bulle maximale et le décalage vertical par rapport à la piste de nettoyage vidéo. Le reste est calculé automatiquement par le composant.

La bulle de chapitres vidéo est contrôlée par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**Propriétés CSS de la bulle de chapitres vidéo**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> largeur max. </p> </td> 
   <td colname="col2"> <p>Largeur maximale de la bulle de chapitres vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> inférieur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Décalage vertical par rapport à la piste de nettoyage vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer une bulle de chapitre vidéo de 235 pixels de large et de huit pixels de haut par rapport au bas de la piste de nettoyage vidéo.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

La bulle de chapitres vidéo se compose d’un en-tête et d’un contenu facultatifs. L’en-tête comporte l’heure de début du chapitre facultative et le titre du chapitre.

L’en-tête est contrôlé par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**Propriétés CSS de l’en-tête de la bulle de chapitre vidéo**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’en-tête de la bulle du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge intérieure du texte de l’en-tête de la bulle du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de l’en-tête de la bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur de ligne <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la ligne de texte de l’en-tête de bulle du chapitre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer un en-tête de bulle de chapitre vidéo d’une hauteur de 22 pixels, une hauteur de ligne de 22 pixels, une marge horizontale de 12 pixels et un arrière-plan gris.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

L’heure de début du chapitre vidéo est contrôlée par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**Propriétés CSS de l’heure de début du chapitre vidéo**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> d’épaisseur de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Épaisseur de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure droite <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre l’heure de début et le titre du chapitre. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer l’heure de début du chapitre à l’aide de la police Verdana grise de dix pixels et dotée d’une marge intérieure de dix pixels à droite.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

Le titre du chapitre vidéo est contrôlé par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**Propriétés CSS du titre du chapitre vidéo**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Couleur du texte du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> d’épaisseur de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Épaisseur de la police du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille de police du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Famille de polices des titres des chapitres vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer un titre de chapitre vidéo qui utilise une police Verdana blanche, en gras et de dix pixels.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

La description du chapitre vidéo est contrôlée par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description
```

**Propriétés CSS de la description du chapitre vidéo**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Couleur du texte de description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur de fond de la description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> d’épaisseur de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Épaisseur de la police de description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille de police de la description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Famille de polices de description des chapitres vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur de ligne <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la ligne de description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de la description du chapitre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer la description d’un chapitre vidéo en utilisant une police Verdana gris foncé de 11 pixels, avec un arrière-plan gris clair. Une hauteur de ligne de cinq pixels, une marge intérieure horizontale de 12 pixels, une marge intérieure supérieure de 12 pixels et une marge intérieure inférieure de neuf pixels.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

Le connecteur de coin situé au bas de la bulle de chapitre est contrôlé par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

**Propriétés CSS du connecteur en coin**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Couleur du connecteur en coin. </p> <p>Défini comme <span class="codeph"> &lt;color&gt; transparent </span> de sorte que seule la couleur de la bordure supérieure soit définie et que les bordures restantes restent transparentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de largeur de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Largeur du connecteur en coin. </p> <p>Défini comme <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> afin que la même largeur soit définie pour les bordures supérieure et horizontale uniquement et que la largeur de la bordure inférieure soit <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Définit uniquement une marge inférieure négative. Elle doit avoir la même valeur que <span class="codeph"> bordure </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer un connecteur en coin gris de six pixels :

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
