---
title: Zoom sur la fenêtre déroulante
description: La vue principale se compose de l’image statique et de l’image agrandie affichées dans la vue déroulante. Elle comprend également la zone de navigation de surbrillance qui s’affiche sur l’image statique, et le message de conseil affiché au-dessus de l’image statique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
TQID: 'https://experienceleague.adobe.com/nQGoCR2S4Qo7lZnvRnzcYhnTWgGZYfYOHfXo1b1kYvE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 655
ht-degree: 0%

---

# Zoom sur la fenêtre déroulante{#flyout-zoom-view}

La vue principale se compose de l’image statique et de l’image agrandie affichées dans la vue déroulante. Elle comprend également la zone de navigation de surbrillance qui s’affiche sur l’image statique, et le message de conseil affiché au-dessus de l’image statique.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de l’image en cours de visualisation ne correspondent pas à celles de la vue zoom déroulante, le contenu de l’image est centré dans la zone d’affichage rectangle de la vue zoom déroulante.

**Propriétés CSS de la vue principale**

L’aspect de la vue principale est contrôlé par le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan de la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre la vue principale transparente :

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Propriétés CSS de la vue déroulante**

L’aspect de la vue déroulante est contrôlé avec le sélecteur de classe CSS suivant :

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
   <td colname="col2"> <p> Position horizontale de la vue déroulante par rapport au coin supérieur gauche de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Position verticale de la vue déroulante par rapport au coin supérieur gauche de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de la vue déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la vue déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Bordure de la vue déroulante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une vue déroulante de 600 x 400 pixels, apparaissant avec 100 pixels décalés à droite de la vue principale de 512 x 288 affichée dans l’exemple précédent :

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Propriétés CSS de la surbrillance dans la vue principale**

L’aspect de la mise en surbrillance dans la vue principale est contrôlé par le sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Il est possible de contrôler l’arrière-plan, la bordure, la transparence et des attributs similaires à l’aide de CSS. Cependant, la taille et la position de l’élément DOM de mise en surbrillance sont gérées par la logique de la visionneuse. Son remplacement par CSS n’est pas pris en charge.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur de la surbrillance. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> d’opacité <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Opacité de surbrillance. </p> <p>Pour Internet Explorer 8, utilisez <span class="codeph"> filter:alpha(opacity-...); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Surbrillance de la bordure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer une mise en surbrillance verte avec 40 % de transparence et une bordure rouge d’un pixel :

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Propriétés CSS du curseur**

Lorsque `highlightmode` paramètre est défini sur `cursor`, les zones de surbrillance dans la vue principale sont remplacées par des illustrations de curseur de taille fixe, qui sont contrôlées par le sélecteur de classe CSS :

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

Il est possible de contrôler l’image et la taille de l’arrière-plan à l’aide de CSS.

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
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Illustration du curseur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du curseur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du curseur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cursor prend en charge le sélecteur d’attributs `input`, qui peut être utilisé pour appliquer différentes illustrations du curseur et tailles pour différents appareils. En particulier, `input="mouse"` correspond aux systèmes de bureau et `input="touch"` correspond aux dispositifs tactiles.

**Propriétés CSS du recouvrement**

Lorsque le paramètre `overlay` est défini sur `1`, la zone entourant le cadre de surbrillance ou l’image du curseur est contrôlée par le sélecteur de classe CSS :

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
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur de recouvrement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> d’opacité <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Opacité du recouvrement. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Propriétés CSS du message de conseil**

L’aspect du message d’info-bulle est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Il est possible de configurer le style, la taille, l’apparence et le décalage vertical de la police à l’aide de CSS. Cependant, l’alignement horizontal est géré par la logique de la visionneuse. Son remplacement par CSS à l’aide de propriétés `left` ou `right` n’est pas pris en charge.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> inférieur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Décalage par rapport au bas de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge intérieure autour du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur de remplissage de l’arrière-plan du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de rayon de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Rayon de bordure en arrière-plan du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> d’opacité <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Opacité de l’arrière-plan du texte du message. </p> <p>Pour Internet Explorer 8, utilisez <span class="codeph"> filtre : alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message de conseil peut être localisé. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) pour plus d’informations.

Exemple - pour configurer un message de conseil semi-transparent avec une police Arial® 12 px blanche, 50 pixels décalés par rapport au bas de la vue principale, un remplissage et une bordure arrondie :

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
