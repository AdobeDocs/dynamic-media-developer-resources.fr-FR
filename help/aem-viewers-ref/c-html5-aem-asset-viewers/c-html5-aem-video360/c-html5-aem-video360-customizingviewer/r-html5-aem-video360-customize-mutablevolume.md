---
description: La commande de volume mutable s'affiche initialement sous la forme d'un bouton qui permet à l'utilisateur de muter ou de désactiver le son du lecteur vidéo.
solution: Experience Manager
title: Volume mutable
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: eb30ea49-e0ae-4ef4-a5b3-e245d96ce0db
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 2%

---

# Volume mutable{#mutable-volume}

La commande de volume mutable s&#39;affiche initialement sous la forme d&#39;un bouton qui permet à l&#39;utilisateur de muter ou de désactiver le son du lecteur vidéo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Lorsqu&#39;un utilisateur survole le bouton, un curseur s&#39;affiche, permettant à l&#39;utilisateur de définir le volume. La commande de volume modifiable peut être dimensionnée, habillée et positionnée, par rapport à la barre de contrôle qui la contient, par CSS.

L&#39;aspect de la zone de volume modifiable est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7mutablevolume
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
   <td colname="col2"> <p> Largeur de la commande de volume mutable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la commande de volume mutable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur de la commande de volume mutable. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’aspect du bouton de mise en sourdine est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7video360viewer .s7mutablevolume .s7mutebutton
```

Vous pouvez contrôler l’image d’arrière-plan de chaque état de bouton. La taille du bouton est héritée de la taille du contrôle de volume.

**Propriétés CSS de l’image de bouton**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les sélecteurs d&#39;attribut `state` et `selected`, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. En particulier, `selected='true'` correspond à l’état &quot;muté&quot; et `selected='false'` correspond à l’état &quot;non muté&quot;.

La zone de la barre de volume verticale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7mutablevolume .s7verticalvolume
```

**Propriétés CSS de la zone de la barre de volume verticale**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Largeur du volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p> Hauteur du volume vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le suivi à l&#39;intérieur du contrôle de volume vertical est contrôlé avec les sélecteurs de classe CSS suivants :

```
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7track 
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**Propriétés CSS de la piste dans le contrôle de volume vertical**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d'arrière-plan de la commande verticale du volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la commande verticale du volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la commande verticale du volume. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton de volume vertical est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7knob
```

**Propriétés CSS du bouton vertical de contrôle du volume**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Illustration du bouton de commande de volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton vertical de commande du volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton vertical de commande du volume. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position horizontale du bouton vertical de commande du volume. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) pour plus d’informations.

**Exemples**  : pour configurer un bouton de mise en sourdine de 32 x 32 pixels et positionné à 6 pixels du haut et à 38 pixels du bord droit de la barre de contrôle. Affichez une image différente pour chacun des quatre états de bouton lorsque vous sélectionnez ou non cette option.

```
.s7video360viewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7video360viewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

Voici un exemple de la façon dont vous pouvez mettre en forme le curseur de volume dans la commande de volume mutable.

```
.s7video360viewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7video360viewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```
