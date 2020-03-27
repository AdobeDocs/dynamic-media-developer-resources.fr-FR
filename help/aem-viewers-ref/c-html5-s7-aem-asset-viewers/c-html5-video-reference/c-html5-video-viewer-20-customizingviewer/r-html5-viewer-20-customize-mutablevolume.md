---
description: Le contrôle du volume mutable s’affiche initialement sous la forme d’un bouton permettant à l’utilisateur de mettre en sourdine ou d’annuler la mise en sourdine du son du lecteur vidéo.
seo-description: Le contrôle du volume mutable s’affiche initialement sous la forme d’un bouton permettant à l’utilisateur de mettre en sourdine ou d’annuler la mise en sourdine du son du lecteur vidéo.
seo-title: Volume muable
solution: Experience Manager
title: Volume muable
topic: Dynamic media
uuid: d7eafff8-dd98-42e2-9d45-e291fe372d8c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Mutable volume{#mutable-volume}

Le contrôle du volume mutable s’affiche initialement sous la forme d’un bouton permettant à l’utilisateur de mettre en sourdine ou d’annuler la mise en sourdine du son du lecteur vidéo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Lorsqu’un utilisateur survole le bouton, un curseur s’affiche pour permettre à l’utilisateur de définir le volume. Le contrôle du volume modifiable peut être dimensionné, habillé et positionné, par rapport à la barre de contrôle qui le contient, par CSS.

L&#39;aspect de la zone de volume modifiable est contrôlé à l&#39;aide du sélecteur de classe CSS suivant :

```
.s7videoviewer .s7mutablevolume
```

**Propriétés CSS du volume modifiable**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure supérieure, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure droite, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur de la commande de volume modifiable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la commande de volume modifiable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur de la commande de volume modifiable. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’aspect du bouton de mise en sourdine est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7videoviewer .s7mutablevolume .s7mutebutton
```

Vous pouvez contrôler l’image d’arrière-plan de chaque état de bouton. La taille du bouton est héritée de la taille du contrôle de volume.

**Propriétés CSS de l’image du bouton**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les sélecteurs `state` et `selected` d’attributs, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. En particulier, `selected='true'` correspond à l’état &quot;muté&quot; et `selected='false'` à l’état &quot;non muté&quot;.

La zone de la barre de volume verticale est contrôlée à l’aide du sélecteur de classe CSS suivant :

```
.s7videoviewer .s7mutablevolume .s7verticalvolume
```

**Propriétés CSS de la zone de la barre de volume verticale**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Hauteur du volume vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le suivi à l&#39;intérieur du contrôle de volume vertical est contrôlé avec les sélecteurs de classe CSS suivants :

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**Propriétés CSS du contrôle vertical du volume**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d'arrière-plan de la commande verticale du volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la commande verticale du volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la commande verticale du volume. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton de volume vertical est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**Propriétés CSS du bouton vertical de contrôle du volume**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p> Illustration du bouton de commande du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton vertical de commande du volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton vertical de commande du volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position horizontale du bouton vertical de contrôle du volume. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

## Exemples {#section-e8caea0a303c425a8a637c2a47c06355}

Pour configurer un bouton de silence de 32 x 32 pixels et positionné à 6 pixels du haut et à 38 pixels du bord droit de la barre de contrôle. Affichez une image différente pour chacun des quatre états de bouton lorsqu’il est sélectionné ou non.

```
.s7videoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

Vous trouverez ci-dessous un exemple de la façon dont vous pouvez mettre en forme le curseur de volume dans le contrôle de volume muable.

```
.s7videoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

Voici un exemple de la manière dont vous pouvez personnaliser le lecteur vidéo afin que le son soit désactivé pendant la lecture. Ajouter le code suivant au code incorporé du lecteur de contenu :

```
                "handlers":{ 
                    "initComplete":function() { 
                        videoViewer.getComponent("mutableVolume").setPosition(0); 
                        videoViewer.getComponent("mutableVolume").deactivate(); 
                    } 
                }
```

Dans l&#39;exemple de code ci-dessus, le niveau de volume est défini sur `0` le `mutableVolume` composant. Ensuite, le même composant est désactivé afin qu’il ne puisse pas être utilisé par l’utilisateur final.
