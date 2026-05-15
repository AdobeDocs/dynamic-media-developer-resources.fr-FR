---
title: Effet de carte graphique
description: En fonction de la valeur du paramètre de mode, la visionneuse affiche des icônes de zone cliquable sur la vue principale aux emplacements où les zones cliquables sont initialement créées dans Dynamic Media Classic ou effectue le rendu de zones exactes qui correspondent à la forme des zones cliquables d’origine.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 873fc387-1d2a-4d74-b85e-fcbb13b691c5
TQID: 'https://experienceleague.adobe.com/cG9m71LkGsy3wqj16qS-pvskuP6J-XrF93jog28I62c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 0%

---

# Effet de carte graphique{#image-map-effect}

En fonction de la valeur du paramètre de mode, la visionneuse affiche des icônes de zone cliquable sur la vue principale aux emplacements où les zones cliquables sont initialement créées dans Dynamic Media Classic ou effectue le rendu de zones exactes qui correspondent à la forme des zones cliquables d’origine.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de l’icône de zone cliquable est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>La classe CSS `s7mapoverlay` utilisée pour appliquer un style aux icônes de zone cliquable dans le passé est désormais obsolète ; utilisez plutôt `s7icon` .

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Icône de zone cliquable illustration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône de zone cliquable en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône de zone cliquable en pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’icône de zone cliquable prend en charge le sélecteur d’attributs de `state`, que vous pouvez utiliser pour appliquer différents habillages aux états d’icône des `default` et des `active`.

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

L’aspect de la zone cliquable est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
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
   <td colname="col1"> <p> </span> d’arrière-plan <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Couleur de remplissage de la zone cliquable. </p> <p>Spécifiée au format #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur de remplissage de la zone cliquable. </p> <p>Spécifiée au format #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Style de bordure de la zone cliquable. </p> <p>Spécifiée comme <span class="codeph"> largeur <span class="varname"> </span> couleur <span class="varname"> pleine </span> </span>, où <span class="codeph"> largeur <span class="varname"> </span> </span> est exprimée en pixels et <span class="codeph"> couleur <span class="varname"> </span> </span> est défini comme #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Configurez une zone cliquable transparente avec `1` bordure noire en pixels :

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
