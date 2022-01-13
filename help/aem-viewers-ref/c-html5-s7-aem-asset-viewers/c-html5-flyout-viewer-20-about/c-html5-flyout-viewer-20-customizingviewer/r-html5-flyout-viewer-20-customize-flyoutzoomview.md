---
title: Zoom déroulant
description: La vue principale se compose de l’image statique et de l’image agrandie affichée dans la vue déroulante. Il comprend également la zone de navigation en surbrillance qui s’affiche sur l’image statique et le message d’info-bulle qui s’affiche au-dessus de l’image statique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 2%

---

# Zoom déroulant{#flyout-zoom-view}

La vue principale se compose de l’image statique et de l’image agrandie affichée dans la vue déroulante. Il comprend également la zone de navigation en surbrillance qui s’affiche sur l’image statique et le message d’info-bulle qui s’affiche au-dessus de l’image statique.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de l’image en cours de visualisation ne correspondent pas aux dimensions du zoom déroulant, le contenu de l’image est centré dans la zone d’affichage rectangle du zoom déroulant.

**Propriétés CSS de la vue principale**

L’aspect de la vue principale est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan de la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour rendre la vue principale transparente :

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Propriétés CSS de la vue déroulante**

L’aspect de la vue déroulante est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale de la vue déroulante, par rapport au coin supérieur gauche de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p> Position verticale de la vue déroulante, par rapport au coin supérieur gauche de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur de la vue déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la vue déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure de la vue déroulante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une vue déroulante à 600 x 400 pixels, apparaissant avec un décalage de 100 pixels à droite de la vue principale de 512 x 288 affichée dans l’exemple précédent :

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Propriétés CSS de la mise en surbrillance dans la vue principale**

L’aspect de la mise en surbrillance dans la vue principale est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Il est possible de contrôler l’arrière-plan, la bordure, la transparence et des attributs similaires à l’aide de CSS. Toutefois, la taille et la position de l’élément DOM de surbrillance sont gérées par la logique de la visionneuse. Le remplacement de l’application par le biais de CSS n’est pas pris en charge.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur du surlignage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p> Mettre l’opacité en surbrillance. </p> <p>Pour Internet Explorer 8, utilisez <span class="codeph"> filter:alpha(opacity-..) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Surlignage de la bordure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une mise en surbrillance verte avec une transparence de 40 % et une bordure rouge d’un pixel :

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Propriétés CSS du curseur**

When `highlightmode` est défini sur `cursor`, les mises en surbrillance se trouvent dans la vue principale et sont remplacées par l’illustration du curseur à taille fixe, qui est contrôlée par le sélecteur de classe CSS :

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

Il est possible de contrôler l’image d’arrière-plan et la taille à l’aide de CSS.

Les propriétés CSS applicables incluent :

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Illustration du curseur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du curseur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du curseur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le curseur prend en charge la fonction `input` le sélecteur d’attributs, qui peut être utilisé pour appliquer une illustration et une taille de curseur différentes pour différents appareils. En particulier, `input="mouse"` correspond aux systèmes de bureau et `input="touch"` correspond aux appareils tactiles.

**Propriétés CSS de la superposition**

Lorsque la variable `overlay` est défini sur `1`, la zone autour du cadre de surbrillance ou de l’image du curseur est contrôlée par le sélecteur de classe CSS :

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de la superposition. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p>Opacité de la superposition. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Propriétés CSS du message de conseil**

L’aspect du message d’info-bulle est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Il est possible de configurer le style, la taille, l’aspect et le décalage vertical de la police au moyen de CSS. Cependant, l’alignement horizontal est géré par la logique de la visionneuse. Le remplacer par CSS à l’aide de `left` ou `right` ne sont pas prises en charge.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Décalage à partir du bas de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure autour du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de fond du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Rayon de la bordure d’arrière-plan du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p>Opacité de l’arrière-plan du texte du message. </p> <p>Pour Internet Explorer 8, utilisez <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message de conseil peut être localisé. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) pour plus d’informations.

Exemple : pour configurer un message d’info-bulle semi-transparent avec une police Arial® de 12 pixels, un décalage de 50 pixels par rapport au bas de l’affichage principal, une marge intérieure et une bordure arrondie :

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
