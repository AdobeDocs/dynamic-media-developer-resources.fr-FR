---
title: Volume mutable
description: La commande de volume modifiable s’affiche initialement sous la forme d’un bouton qui permet à l’utilisateur de couper ou d’activer le son du lecteur vidéo de recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e0a3e849-842b-4137-acc2-34301e89518f
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# Volume mutable{#mutable-volume}

La commande de volume modifiable s’affiche initialement sous la forme d’un bouton qui permet à l’utilisateur de couper ou d’activer le son du lecteur vidéo de recadrage intelligent.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Lorsqu’un utilisateur survole le bouton, un curseur s’affiche pour lui permettre de définir le volume. Le contrôle de volume modifiable peut être dimensionné, doté d&#39;une enveloppe et positionné par rapport à la barre de contrôle qui le contient, à l&#39;aide de CSS.

L’aspect de la zone de volume modifiable est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7mutablevolume
```

**Propriétés CSS du volume modifiable**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure droite, marge intérieure incluse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du contrôle de volume modifiable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du contrôle de volume modifiable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur de la commande de volume modifiable. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’aspect du bouton Silence/Son réactivé est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton
```

Vous pouvez contrôler l’image d’arrière-plan pour chaque état de bouton. La taille du bouton est héritée de la taille du contrôle de volume.

**Propriétés CSS de l’image du bouton**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les sélecteurs d&#39;attributs `state` et `selected`, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. En particulier, `selected='true'` correspond à l&#39;état « muted » et `selected='false'` correspond à l&#39;état « unmuted ».

La zone de la barre de volume verticale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume
```

**Propriétés CSS de la zone de la barre de volume verticale**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d'arrière-plan du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p> Hauteur du volume vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

La piste à l’intérieur du contrôle du volume vertical est contrôlée avec les sélecteurs de classe CSS suivants :

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**Propriétés CSS de la commande de volume vertical**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d'arrière-plan de la commande de volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la commande de volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la commande de volume vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton de volume vertical est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**Propriétés CSS du bouton de réglage du volume vertical**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Illustration du bouton de contrôle du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton de réglage du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton de réglage du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position horizontale du bouton de réglage du volume vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) pour plus d’informations.

## Exemples {#section-e8caea0a303c425a8a637c2a47c06355}

Pour configurer un bouton de désactivation du son de 32 x 32 pixels et positionné à 6 pixels du haut et à 38 pixels du bord droit de la barre de contrôle. Affichez une image différente pour chacun des quatre états de bouton différents, qu’ils soient sélectionnés ou non.

```
.s7smartcropvideoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

Voici un exemple de mise en forme du curseur de volume dans le contrôle de volume modifiable.

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

Voici un exemple de personnalisation du lecteur vidéo pour que le son soit désactivé lors de la lecture. Ajoutez le code suivant au code incorporé de la visionneuse :

```
                "handlers":{ 
                    "initComplete":function() { 
                        videoViewer.getComponent("mutableVolume").setPosition(0); 
                        videoViewer.getComponent("mutableVolume").deactivate(); 
                    } 
                }
```

Dans l’exemple de code ci-dessus, le niveau de volume est défini sur `0` sur le composant `mutableVolume`. Ensuite, le même composant est désactivé et ne peut donc pas être utilisé par l’utilisateur final ou l’utilisatrice finale.
