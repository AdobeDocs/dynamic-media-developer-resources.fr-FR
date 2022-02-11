---
title: Défilement vidéo
description: La barre de défilement vidéo est la commande de curseur horizontale qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 2%

---

# Défilement vidéo{#video-scrubber}

La barre de défilement vidéo est la commande de curseur horizontale qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barre de défilement se déplace également au fur et à mesure que la vidéo est lue pour indiquer la position de l’heure actuelle de la vidéo pendant la lecture. La barre de défilement vidéo prend toujours toute la largeur de la barre de contrôle. Il est possible d’appliquer un habillage à la barre de défilement vidéo et de modifier sa hauteur et sa position verticale, par CSS.

L’aspect général de la barre de défilement vidéo est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**Propriétés CSS de la barre de défilement vidéo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure inférieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de défilement vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de la barre de défilement vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les sélecteurs de classe CSS suivants effectuent le suivi des indicateurs d’arrière-plan, de lecture et de chargement :

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**Propriétés CSS du suivi**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du suivi correspondant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du suivi correspondant. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Décalage vertical des boutons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Obtenir une illustration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle la bulle de durée de lecture :

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**Propriétés CSS de la bulle de durée de lecture**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Famille de polices à utiliser pour l’affichage du texte temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Taille de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Couleur de police à utiliser pour le texte d’affichage de l’heure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de la zone bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Illustrations à bulles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement de texte </span> </p> </td> 
   <td colname="col2"> <p>Alignement du texte avec la zone de bulle. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle de la barre de défilement vidéo peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) pour plus d’informations.

**Exemple** - Pour configurer une visionneuse de vidéos avec une barre de défilement vidéo avec des couleurs de suivi personnalisées. La barre de défilement doit mesurer dix pixels de haut et positionner dix pixels et 35 pixels à partir des bords supérieur et gauche de la barre de contrôle.

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

Lorsque la fonction de chapitre vidéo est activée avec la fonction `navigation` , les emplacements de chapitre s’affichent sous la forme de marqueurs au-dessus du suivi de la barre de défilement vidéo.

Le marqueur de chapitre vidéo est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**Propriétés CSS du marqueur de chapitre vidéo**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du marqueur de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du marqueur du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Illustration du marqueur du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les deux `state` sélecteur d’attributs que vous pouvez utiliser pour appliquer différents habillages à différents états de bouton. En particulier, `selected='default'` correspond à l’état par défaut du marqueur de chapitre vidéo et `selected='over'` est utilisé lorsque le marqueur de chapitre vidéo est activé par le survol ou le toucher de la souris.

**Exemple** - Pour configurer un marqueur de chapitre vidéo de 5 x 8 pixels et utiliser des illustrations différentes pour l’état &quot;par défaut&quot; et &quot;sur&quot;.

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

La bulle de chapitre vidéo est positionnée au-dessus du marqueur de chapitre vidéo et affiche le titre, l’heure de début et la description d’un chapitre donné. Il est possible de contrôler la largeur maximale de la bulle et le décalage vertical par rapport au suivi de la barre de défilement vidéo. Le reste est calculé automatiquement par le composant.

La bulle de chapitre vidéo est contrôlée par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**Propriétés CSS de la bulle de chapitre vidéo**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>Largeur maximale de la bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Décalage vertical à partir de la piste de défilement vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer une bulle de chapitre vidéo d’une largeur de 235 pixels et d’une hauteur de huit pixels au bas du suivi de la barre de défilement vidéo.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

La bulle de chapitre vidéo se compose d’un en-tête et d’un contenu facultatifs. L’en-tête comporte l’heure de début et le titre facultatifs du chapitre.

L’en-tête est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**Propriétés CSS de l’en-tête de bulle de chapitre vidéo**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’en-tête de la bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure du texte de l’en-tête de la bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de l’en-tête de la bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la ligne de texte de l’en-tête de la bulle de chapitre vidéo. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Poids de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge intérieure-droite </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre l’heure de début et le titre du chapitre. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer l’heure de début du chapitre à l’aide de la police Verdana grise de dix pixels et d’une marge intérieure de dix pixels à droite.

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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur de texte du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Poids de police du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices du titre du chapitre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer un titre de chapitre vidéo qui utilise une police Verdana blanche, gras et de dix pixels.

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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur de texte de description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Poids de police de la description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police de la description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices de description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de ligne de description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de la description du chapitre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer la description du chapitre vidéo à l’aide d’une police Verdana de 11 pixels de gris foncé, avec un arrière-plan gris clair. Enfin, utilise une hauteur de ligne de cinq pixels, une marge intérieure horizontale de 12 pixels, une marge intérieure supérieure de 12 pixels et une marge intérieure inférieure de neuf pixels.

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

Le connecteur de coin au bas de la bulle de chapitre est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**Propriétés CSS du connecteur de décalage**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du connecteur de décalage. </p> <p>Défini comme <span class="codeph"> &lt;color&gt; transparent </span> afin que seule la couleur de la bordure supérieure soit définie et que les bordures restantes restent transparentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du connecteur de décalage. </p> <p>Défini comme <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> de sorte que la même largeur soit définie pour les bordures supérieure et horizontale uniquement et que la largeur de la bordure inférieure soit <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Définit une marge inférieure négative uniquement. Elle doit avoir la même valeur que <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer un connecteur de décalage de six pixels gris :

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
