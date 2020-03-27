---
description: Le principal est constitué de l’image statique, de l’image agrandie affichée dans le de fenêtre déroulante, de la zone de navigation en surbrillance affichée sur l’image statique et du message d’info-bulle affiché au-dessus de l’image statique.
seo-description: Le principal est constitué de l’image statique, de l’image agrandie affichée dans le de fenêtre déroulante, de la zone de navigation en surbrillance affichée sur l’image statique et du message d’info-bulle affiché au-dessus de l’image statique.
seo-title: de zoom déroulant
solution: Experience Manager
title: de zoom déroulant
topic: Dynamic media
uuid: 35c60228-3044-442b-a8e2-e13d0bd306a5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Flyout zoom view{#flyout-zoom-view}

Le principal est constitué de l’image statique, de l’image agrandie affichée dans le de fenêtre déroulante, de la zone de navigation en surbrillance affichée sur l’image statique et du message d’info-bulle affiché au-dessus de l’image statique.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de l’image affichée ne correspondent pas aux dimensions du de zoom déroulant, le contenu de l’image est centré dans la zone d’affichage du de zoom déroulant  rectangle.

**Propriétés CSS du principal**

L’aspect du principal est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du  principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour rendre le principal transparent :

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Propriétés CSS du déroulant**

L’aspect du de fenêtre déroulante est contrôlé par le sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale du  de fenêtre déroulante, par rapport au coin supérieur gauche du principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p> Position verticale du  de fenêtre déroulante, par rapport au coin supérieur gauche du principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du  de fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du  de fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure du de fenêtre déroulante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un de fenêtre déroulante  à 600 x 400 pixels, avec un décalage de 100 pixels à droite du principal de 512 x 288  illustré dans l’exemple précédent :

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Propriétés CSS de la mise en surbrillance dans le principal**

L’aspect de la mise en surbrillance dans le principal est contrôlé par le sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Il est possible de contrôler l’arrière-plan, la bordure, la transparence et des attributs similaires à l’aide de CSS. Toutefois, la taille et la position de l’élément DOM de mise en surbrillance sont gérées par la logique du lecteur. Il n’est pas possible de le remplacer par CSS.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur de la mise en surbrillance. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p> Mettez en surbrillance l’opacité. </p> <p>Pour Internet Explorer 8, utilisez <span class="codeph"> filter:alpha(opacity-...); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Surlignage de la bordure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer la mise en surbrillance verte avec une transparence de 40 % et une bordure rouge d’un pixel :

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Propriétés CSS du curseur**

Lorsque le `highlightmode` paramètre est défini sur `cursor`, les mises en surbrillance se trouvent dans le principal et sont remplacées par une illustration de curseur de taille fixe, qui est contrôlée par le sélecteur de classe CSS :

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

Il est possible de contrôler l’image d’arrière-plan et la taille à l’aide de CSS.

Les propriétés CSS applicables sont les suivantes :

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
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
>Le curseur prend en charge le sélecteur d’ `input` attributs, qui peut être utilisé pour appliquer une illustration et une taille différentes aux différents périphériques. En particulier, `input="mouse"` correspond aux systèmes de bureau et `input="touch"` aux périphériques tactiles.

**Propriétés CSS de l’incrustation**

Lorsque le `overlay` paramètre est défini sur `1`, la zone entourant le cadre de surbrillance ou l’image du curseur est contrôlée par le sélecteur de classe CSS :

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’incrustation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p>Opacité du recouvrement. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Propriétés CSS du message de conseil**

L’aspect du message de conseil est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Il est possible de configurer le style de police, l’aspect de la taille et le décalage vertical au moyen de CSS. Toutefois, l’alignement horizontal est géré par la logique du lecteur de contenu. Il n’est pas possible de le remplacer via CSS à l’aide de `left` ou de `right` propriétés.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Décalage à partir du bas du  principal. </p> </td> 
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
   <td colname="col2"> <p>Remplissage autour du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de fond du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Rayon de bordure d’arrière-plan du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p>Opacité d’arrière-plan du texte du message. </p> <p>Pour Internet Explorer 8, utilisez <span class="codeph"> filter:alpha(opacity-...) ). </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message d’info-bulle peut être localisé. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) de l’interface utilisateur.

Exemple : pour configurer un message d’info-bulle semi-transparent avec une police Arial blanche de 12 px, un décalage de 50 pixels par rapport au bas du principal, un remplissage et une bordure arrondie :

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

