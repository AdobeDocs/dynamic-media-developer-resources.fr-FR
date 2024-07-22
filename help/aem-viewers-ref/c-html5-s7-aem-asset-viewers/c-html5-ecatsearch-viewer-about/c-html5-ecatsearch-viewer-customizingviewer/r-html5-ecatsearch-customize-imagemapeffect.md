---
title: Effet de zone cliquable
description: Selon la valeur du paramètre de mode, la visionneuse affiche les icônes de zone cliquable sur la vue principale à des endroits où les zones cliquables sont créées à l’origine dans Dynamic Media Classic ou effectue le rendu des zones exactes qui correspondent à la forme des zones cliquables d’origine.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 873fc387-1d2a-4d74-b85e-fcbb13b691c5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Effet de zone cliquable{#image-map-effect}

Selon la valeur du paramètre de mode, la visionneuse affiche les icônes de zone cliquable sur la vue principale à des endroits où les zones cliquables sont créées à l’origine dans Dynamic Media Classic ou effectue le rendu des zones exactes qui correspondent à la forme des zones cliquables d’origine.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de l’icône de zone cliquable est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>La classe CSS `s7mapoverlay` utilisée par le passé pour mettre en forme les icônes de zone cliquable est désormais obsolète. Utilisez `s7icon` à la place.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Illustration de l’icône de zone cliquable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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
>L’icône de zone cliquable prend en charge le sélecteur d’attributs `state`, que vous pouvez utiliser pour appliquer différents habillages aux états d’icônes de `default` et `active`.

Exemple : configurez une icône de zone cliquable de 28 x 28 pixels qui affiche une image différente pour chacun des deux états d’icône différents.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Voir aussi [Prise en charge des zones cliquables](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

L’aspect de la zone cliquable est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur de remplissage de la zone cliquable. </p> <p>Spécifié au format #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Couleur de remplissage de la zone cliquable. </p> <p>Spécifié au format #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p> Style de bordure de la zone cliquable. </p> <p>Spécifié en tant que <span class="codeph"> <span class="varname"> width </span> solid <span class="varname"> color </span> </span>, où <span class="codeph"> <span class="varname"> width </span> </span> est exprimé en pixels et <span class="codeph"> <span class="varname"> color </span> </span> est défini sur #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez une zone de zone cliquable transparente avec une bordure noire de `1` pixels :

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
