---
description: La barre de défilement de la vidéo est le curseur horizontal qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.
seo-description: La barre de défilement de la vidéo est le curseur horizontal qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.
seo-title: Nettoyage vidéo
solution: Experience Manager
title: Nettoyage vidéo
topic: Dynamic media
uuid: 5e4abc8a-ee61-4528-a5de-66148aac3389
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video scrubber{#video-scrubber}

La barre de défilement de la vidéo est le curseur horizontal qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Le bouton de défilement se déplace également pendant la lecture de la vidéo pour indiquer la position temporelle actuelle de la vidéo pendant la lecture. La barre de défilement vidéo occupe toujours toute la largeur de la barre de contrôle. Il est possible d’habiller la barre de défilement vidéo. modifier sa hauteur et sa position verticale, par CSS.

L’aspect général de la barre de défilement vidéo est contrôlé par le sélecteur de classe CSS suivant :

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
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure inférieure, y compris le remplissage. </p> </td> 
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
   <td colname="col2"> <p>Hauteur de la piste correspondante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p>Touchez l’illustration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle la bulle de temps de lecture :

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**Propriétés CSS de la bulle de temps de lecture**

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
   <td colname="col2"> <p> Couleur de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p>Des illustrations à bulles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Alignement du texte sur la zone de bulle. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle de la barre de défilement vidéo peut être localisée. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

**Exemple** : pour configurer une visionneuse de vidéos avec un défilement vidéo avec des couleurs de suivi personnalisées de 10 pixels de haut et positionnées à 10 pixels et 35 pixels à partir des bords supérieur et gauche de la barre de contrôle.

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

Lorsque le `navigation` paramètre permet d’activer le chapitrage vidéo, les emplacements de chapitre sont affichés sous forme de marqueurs au-dessus de la piste de défilement vidéo.

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
   <td colname="col2"> <p>Hauteur du marqueur de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p>Illustration du marqueur de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’ `state` attributs, que vous pouvez utiliser pour appliquer différents habillages à différents états de bouton. En particulier, `selected='default'` correspond à l’état par défaut du marqueur de chapitre vidéo et `selected='over'` est utilisé lorsque le marqueur de chapitre vidéo est activé par un mouvement de survol ou de toucher de la souris.

**Exemple** : pour configurer une marque de chapitre vidéo de 5 x 8 pixels et utiliser des illustrations différentes pour les états &quot;par défaut&quot; et &quot;sur&quot;.

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

La bulle de chapitre vidéo est placée au-dessus du marqueur de chapitre vidéo et affiche le titre, l’heure  et la description d’un chapitre donné. Il est possible de contrôler la largeur maximale de la bulle et le décalage vertical par rapport à la piste de défilement vidéo. Le reste est calculé automatiquement par le composant.

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

**Exemple** : pour configurer une bulle de chapitre vidéo de 235 pixels de large et de 8 pixels de haut en bas de la piste de défilement vidéo.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

La bulle de chapitre vidéo se compose d’un en-tête et d’un contenu facultatifs. L’en-tête comporte l’heure et le titre facultatifs du de chapitre  l’heure et le titre du chapitre.

L’en-tête est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**Propriétés CSS de l’en-tête de bulle de chapitre vidéo**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’en-tête de bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure du texte d’en-tête de bulle de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de l’en-tête de bulle du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la ligne de texte de l’en-tête de bulle du chapitre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** : pour configurer un en-tête de bulle de chapitre vidéo de 22 pixels de haut, une hauteur de ligne de 22 pixels, une marge horizontale de 12 pixels et un arrière-plan gris.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

L’heure  du chapitre vidéo est contrôlée par le sélecteur de classe CSS suivant :

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**Propriétés CSS du de chapitre vidéo  l’heure**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font- </span> </p> </td> 
   <td colname="col2"> <p> de police. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> remplissage-droit </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre l’heure  du et le titre du chapitre. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** : pour configurer le temps de de chapitres à l’aide de la police Verdana grise de 10 pixels et d’un remplissage de 10 pixels à droite.

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
   <td colname="col2"> <p>Couleur du texte du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font- </span> </p> </td> 
   <td colname="col2"> <p> de polices de titre de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police du titre du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices de titre de chapitre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** : pour configurer un titre de chapitre vidéo qui utilise une police Verdana blanche, en gras, de dix pixels.

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
   <td colname="col2"> <p>Couleur du texte de description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font- </span> </p> </td> 
   <td colname="col2"> <p> de police de description de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police de la description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices de description de chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la ligne de description du chapitre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de description du chapitre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** : pour configurer la description du chapitre vidéo à l’aide d’une police Verdana de 11 pixels gris foncé, avec un arrière-plan gris clair ; Hauteur de ligne de 5 pixels, remplissage horizontal de 12 pixels, remplissage supérieur de 12 pixels et remplissage inférieur de 9 pixels.

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

Le connecteur de coin situé au bas de la bulle de chapitre est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**Propriétés CSS du connecteur de coin**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du connecteur de coin. </p> <p>Défini comme transparent <span class="codeph"> &lt;color&gt; </span> afin que seule la couleur de bordure supérieure soit définie et que les bordures restantes restent transparentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du connecteur de coin. </p> <p>Défini comme <span class="codeph"> &lt;largeur&gt; &lt;largeur&gt; 0 </span> de sorte que la même largeur soit définie pour les bordures supérieure et horizontale uniquement et que la largeur de la bordure inférieure soit <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Définit uniquement une marge inférieure négative. Elle doit avoir la même valeur que celle de <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer un connecteur de coin gris de six pixels :

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

