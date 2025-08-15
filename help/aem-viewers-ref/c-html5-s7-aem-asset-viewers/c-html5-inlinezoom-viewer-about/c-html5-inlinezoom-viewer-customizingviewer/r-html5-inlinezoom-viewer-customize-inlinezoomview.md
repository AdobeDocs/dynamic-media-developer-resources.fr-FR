---
title: Affichage de zoom déroulant
description: La vue principale se compose de l’image statique et de l’image agrandie affichée dans la vue déroulante au-dessus de l’image statique. Il se compose également du message de conseil affiché au-dessus de l’image statique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Affichage de zoom déroulant{#flyout-zoom-view}

La vue principale se compose de l’image statique et de l’image agrandie affichée dans la vue déroulante au-dessus de l’image statique. Il se compose également du message de conseil affiché au-dessus de l’image statique.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

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

Le message du conseil peut être localisé. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) de l’interface utilisateur.

.

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
