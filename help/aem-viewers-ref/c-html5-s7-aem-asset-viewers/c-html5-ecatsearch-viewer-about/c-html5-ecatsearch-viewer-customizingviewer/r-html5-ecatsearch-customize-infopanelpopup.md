---
description: La fenêtre contextuelle du panneau d’informations s’affiche au milieu de la zone de la visionneuse lorsqu’un utilisateur active une zone cliquable dont la propriété rollover_key est définie dans Scene7 Publishing System et si la fonctionnalité du panneau d’informations est correctement configurée pour la visionneuse.
seo-description: La fenêtre contextuelle du panneau d’informations s’affiche au milieu de la zone de la visionneuse lorsqu’un utilisateur active une zone cliquable dont la propriété rollover_key est définie dans Scene7 Publishing System et si la fonctionnalité du panneau d’informations est correctement configurée pour la visionneuse.
seo-title: Fenêtre contextuelle du panneau d’informations
solution: Experience Manager
title: Fenêtre contextuelle du panneau d’informations
topic: Dynamic media
uuid: a5c50e54-1ea7-4908-a8a5-dbeea5c8eabb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Fenêtre contextuelle du panneau d’informations{#info-panel-popup}

La fenêtre contextuelle du panneau d’informations s’affiche au milieu de la zone de la visionneuse lorsqu’un utilisateur active une zone cliquable dont la propriété rollover_key est définie dans Scene7 Publishing System et si la fonctionnalité du panneau d’informations est correctement configurée pour la visionneuse.

L’arrière-plan du panneau d’informations couvre toute la zone de la visionneuse et est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7infopanelpopup .s7backoverlay`

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
   <td colname="col2"> <p>Remplir l’arrière-plan du panneau d’informations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez la fenêtre contextuelle du panneau d’informations pour utiliser un arrière-plan noir semi-transparent.

```
.s7ecatalogsearchviewer .s7infopanelpopup .s7backoverlay { 
 background-color : rgba(0,0,0,0.75); 
}
```

La boîte de dialogue du panneau d’informations s’affiche par défaut au milieu de la zone de visualisation. Cependant, il est possible de contrôler sa taille, son alignement, son arrière-plan et sa bordure avec le sélecteur de classe CSS.

`.s7ecatalogsearchviewer .s7infopanelpopup .s7overlay`

<table id="table_4E666A03A3D44CEEA72225113553AB3F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position horizontale de la boîte de dialogue du panneau d’informations dans le fond du panneau de zone de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position verticale de la boîte de dialogue du panneau d’informations dans la zone de visualisation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-gauche </span> </p> </td> 
   <td colname="col2"> <p>La marge gauche de la boîte de dialogue du panneau d’informations peut être utilisée à des fins de centrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-haut </span> </p> </td> 
   <td colname="col2"> <p>La marge supérieure de la boîte de dialogue du panneau d’informations peut être utilisée à des fins de centrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Rayon de la bordure de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Ombre de la boîte de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez une boîte de dialogue du panneau d’informations de 300 x 200 pixels centrée dans la zone de visualisation ; possède un remplissage de 40 pixels en haut et de 10 pixels sur tous les autres côtés, un arrière-plan gris clair et un rayon de bordure de 10 pixels et une ombre portée.

```
.s7ecatalogsearchviewer .s7infopanelpopup .s7overlay { 
 left: 50%; 
 top: 50%; 
 margin-left: -150px; 
 margin-top: -100px; 
 width: 300px; 
 height: 200px; 
 padding-top: 40px; 
 padding-right: 10px; 
 padding-bottom: 10px; 
 padding-left: 10px; 
 background-color:rgb(221,221,221); 
 border-radius: 10px 10px 10px 10px; 
box-shadow: 0 0 5px rgba(0,0,0,0.25);  
}
```

La boîte de dialogue du panneau d’informations est dotée d’un bouton de fermeture, et le fait de cliquer ou d’appuyer sur ce bouton ferme la boîte de dialogue.

L’aspect de ce bouton est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’ `state` attributs, que vous pouvez utiliser pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

Exemple : pour configurer un bouton de fermeture de boîte de dialogue de 28 x 28 pixels, positionné à 5 pixels du bord supérieur et droit de la boîte de dialogue du panneau d’informations, et affiche une image différente pour chacun des quatre états de bouton.

```
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton { 
 width: 28px; 
 height: 28px; 
 top: 5px; 
 right: 5px; 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="up"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="over"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="down"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="disabled"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
}
```

