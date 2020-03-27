---
description: En fonction de la valeur du paramètre de mode, la visionneuse affiche les icônes de zone cliquable sur le principal aux endroits où les zones cliquables sont créées à l’origine dans Scene7 Publishing System ou restitue les zones exactes qui correspondent à la forme des zones cliquables d’origine.
seo-description: En fonction de la valeur du paramètre de mode, la visionneuse affiche les icônes de zone cliquable sur le principal aux endroits où les zones cliquables sont créées à l’origine dans Scene7 Publishing System ou restitue les zones exactes qui correspondent à la forme des zones cliquables d’origine.
seo-title: Effet de zone cliquable
solution: Experience Manager
title: Effet de zone cliquable
topic: Dynamic media
uuid: 193d2f4e-77a2-4741-bf36-90ca31c600c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Image map effect{#image-map-effect}

En fonction de la valeur du paramètre de mode, la visionneuse affiche les icônes de zone cliquable sur le principal aux endroits où les zones cliquables sont créées à l’origine dans Scene7 Publishing System ou restitue les zones exactes qui correspondent à la forme des zones cliquables d’origine.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de l’icône de zone cliquable est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>La classe `s7mapoverlay` CSS utilisée dans le passé pour mettre en forme les icônes de zone cliquable est désormais obsolète ; utilisez plutôt `s7icon` .

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p>Illustration de l’icône de zone cliquable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône de zone cliquable en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône de zone cliquable en pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’icône de zone cliquable prend en charge le sélecteur d’ `state` attributs, que vous pouvez utiliser pour appliquer différents habillages aux états d’icône `default` et `active`.

Exemple : configurez une icône de zone cliquable de 28 x 28 pixels qui affiche une image différente pour chacun des deux états d’icône différents.

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Voir aussi prise en charge [des zones](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)cliquables.

L’aspect de la région de zone cliquable est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur de remplissage de la zone cliquable. </p> <p>Spécifié au format #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur de remplissage de la zone cliquable. </p> <p>Spécifié au format #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p> Style de bordure de la zone cliquable. </p> <p>Spécifié comme <span class="codeph"> couleur <span class="varname"> unie </span> de largeur <span class="varname"> , où </span> </span><span class="codeph"> la largeur  est exprimée en pixels et le de couleur de est défini comme #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A).<span class="varname"></span></span><span class="codeph"><span class="varname"></span></span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez une zone de zone cliquable transparente avec une bordure noire `1` en pixels :

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

