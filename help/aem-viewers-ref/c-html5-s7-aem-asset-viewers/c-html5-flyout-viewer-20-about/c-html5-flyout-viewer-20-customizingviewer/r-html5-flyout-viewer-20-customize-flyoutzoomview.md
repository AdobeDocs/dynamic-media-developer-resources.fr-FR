---
title: Affichage de zoom déroulant
description: La vue principale se compose de l’image statique et de l’image agrandie affichée dans la vue déroulante. Il comprend également la zone de navigation de mise en surbrillance affichée sur l’image statique et le message de conseil affiché au-dessus de l’image statique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Affichage de zoom déroulant{#flyout-zoom-view}

La vue principale se compose de l’image statique et de l’image agrandie affichée dans la vue déroulante. Il comprend également la zone de navigation de mise en surbrillance affichée sur l’image statique et le message de conseil affiché au-dessus de l’image statique.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de l’image affichée ne correspondent pas aux dimensions de la vue de zoom déroulante, le contenu de l’image est centré dans la zone d’affichage rectangulaire de la vue de zoom déroulante.

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
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
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

L’aspect de la vue déroulante est contrôlé par le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> Gauche </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale de la vue déroulante par rapport au coin supérieur gauche de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p> Position verticale de la vue déroulante par rapport au coin supérieur gauche de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de la vue Fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la vue déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> frontière </span> </p> </td> 
   <td colname="col2"> <p>Bordure de la vue déroulante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une vue déroulante à 600 x 400 pixels, apparaissant avec un décalage de 100 pixels à droite de la vue principale de 512 x 288 illustrée dans l’exemple précédent :

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Propriétés CSS du surlignage dans la vue principale**

L’aspect de la mise en surbrillance dans la vue principale est contrôlé par le sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Il est possible de contrôler l’arrière-plan, la bordure, la transparence et des attributs similaires à l’aide de CSS. Toutefois, la taille et la position de l’élément DOM de mise en surbrillance sont gérées par la logique de la visionneuse. Le remplacement par CSS n’est pas pris en charge.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur du surlignage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p> Mettez en surbrillance l’opacité. </p> <p>Pour Internet Explorer 8, utilisez <span class="codeph"> filter :alpha(opacité-...) ) ; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> frontière </span> </p> </td> 
   <td colname="col2"> <p>Mise en surbrillance de la bordure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour définir un surlignage vert avec une transparence de 40 % et une bordure rouge d’un pixel :

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Propriétés CSS du curseur**

Lorsque `highlightmode` le paramètre est défini sur `cursor`, mettre en surbrillance sont dans la vue principale est remplacé par une illustration de curseur de taille fixe, qui est contrôlée par le sélecteur de classe CSS :

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
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Illustration du curseur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du curseur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du curseur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le curseur prend en charge le sélecteur d’attributs `input` , qui peut être utilisé pour appliquer différentes illustrations et tailles de curseur pour différents périphériques. En particulier, `input="mouse"` correspond aux systèmes de bureau et `input="touch"` correspond aux appareils tactiles.

**Propriétés CSS du recouvrement**

Lorsque le `overlay` paramètre est défini sur `1`, la zone autour du cadre de surbrillance ou de l’image du curseur est contrôlée à l’aide du sélecteur de classe CSS :

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
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur de recouvrement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p>Opacité du recouvrement. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Propriétés CSS du message de conseil**

L’aspect du message de conseil est contrôlé par le sélecteur de classe CSS suivant :

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Il est possible de configurer le style, la taille, l’apparence et le décalage vertical de la police via CSS. Toutefois, l’alignement horizontal est géré par la logique de la visionneuse. Il n’est pas possible de le remplacer par le biais de CSS à l’aide `left` des propriétés OR `right` .

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p>Décalage par rapport au bas de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure autour du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur de fond du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rayon de bordure </span> </p> </td> 
   <td colname="col2"> <p>Rayon de bordure d’arrière-plan du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p>Opacité d’arrière-plan du texte du message. </p> <p>Pour Internet Explorer 8, utilisez <span class="codeph"> filter :alpha(opacité-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message du conseil peut être localisé. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) de l’interface utilisateur.

Exemple : pour configurer un message de conseil semi-transparent avec une police Arial® blanche 12 px, décalée de 50 pixels par rapport au bas de la vue principale, une marge intérieure et une bordure arrondie :

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
