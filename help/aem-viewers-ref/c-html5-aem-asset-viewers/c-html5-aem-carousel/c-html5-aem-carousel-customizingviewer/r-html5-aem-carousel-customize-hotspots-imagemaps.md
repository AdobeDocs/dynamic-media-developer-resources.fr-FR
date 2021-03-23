---
description: Le lecteur affiche des icônes de zones réactives sur la vue principale dans les endroits où des zones réactives ont été créées à l’origine dans Dynamic Media of AEM Assets - à la demande.
seo-description: Le lecteur affiche des icônes de zones réactives sur la vue principale dans les endroits où des zones réactives ont été créées à l’origine dans Dynamic Media of AEM Assets - à la demande.
seo-title: Zones réactives et zones cliquables
solution: Experience Manager
title: Zones réactives et zones cliquables
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
feature: Dynamic Media Classic, Visionneuses, SDK/API, Bannières de carrousel
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 1%

---


# Zones réactives et zones cliquables{#hotspots-and-image-maps}

Le lecteur affiche des icônes de zones réactives sur la vue principale dans les endroits où des zones réactives ont été créées à l’origine dans Dynamic Media of AEM Assets - à la demande.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visualisation principale**

L’aspect de l’icône de zone réactive est contrôlé par le sélecteur de classe CSS suivant :

```
.s7carouselviewer .s7imagemapeffect .s7icon
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
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Image d’icône de zone réactive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p>Positionnez l’objet d’illustration à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône de zone réactive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône de zone réactive. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez une icône de zone réactive de 56 x 56 pixels qui affiche une image différente pour chacun des deux états d’icône différents :

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**Propriétés CSS de la zone de zone cliquable**

L’aspect de la région de zone cliquable est contrôlé par le sélecteur de classe CSS suivant :

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière  </span> </p> </td> 
   <td colname="col2"> <p>Couleur de remplissage de la zone de zone cliquable. </p> <p>Spécifiez cette couleur aux formats <span class="codeph"> #RRGBB </span>, <span class="codeph"> RGB(R, G, B) </span> ou <span class="codeph"> RGBA(R, G, B, A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur de remplissage de la zone de zone cliquable. </p> <p>Spécifiez cette couleur aux formats <span class="codeph"> #RRGBB </span>, <span class="codeph"> RGB(R, G, B) </span> ou <span class="codeph"> RGBA(R, G, B, A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p> Style de bordure de la zone de zone de zone cliquable. Doit être spécifié comme " <span class="codeph"> width </span> <span class="codeph"> solid color </span>", où <span class="codeph"> width </span> est exprimé en pixels et <span class="codeph"> color </span> est défini comme <span class="codeph"> #RRGBB </span>, <span class="codeph"> RGB(R, G, B) &lt;a1 1/&gt; ou <span class="codeph"> RGBA(R, G, B, A) </span>.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez une zone transparente de zone cliquable avec une bordure noire d’un pixel :

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

