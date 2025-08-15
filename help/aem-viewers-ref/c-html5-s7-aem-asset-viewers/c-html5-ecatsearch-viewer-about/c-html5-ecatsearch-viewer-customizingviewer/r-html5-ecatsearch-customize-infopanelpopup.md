---
title: Fenêtre contextuelle du panneau d’informations
description: La fenêtre contextuelle du panneau d’informations s’affiche au milieu de la zone de visionneuse lorsqu’un utilisateur active une zone cliquable dont la propriété rollover_key est définie dans Dynamic Media Classic et si la fonctionnalité de panneau d’informations est correctement configurée pour la visionneuse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 907b7bd5-3f87-4918-ad62-8a28249ea023
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Fenêtre contextuelle du panneau d’informations{#info-panel-popup}

La fenêtre contextuelle du panneau d’informations s’affiche au milieu de la zone de visionneuse lorsqu’un utilisateur active une zone cliquable dont la propriété rollover_key est définie dans Dynamic Media Classic et si la fonctionnalité de panneau d’informations est correctement configurée pour la visionneuse.

L’arrière-plan du panneau d’informations couvre toute la zone de la visionneuse et est contrôlé par le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Remplissage de l’arrière-plan du panneau d’informations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés.</p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Configurez la fenêtre contextuelle du panneau d’informations pour utiliser un arrière-plan noir semi-transparent.

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
   <td colname="col1"> <p> <span class="codeph"> Gauche </span> </p> </td> 
   <td colname="col2"> <p>Position horizontale de la boîte de dialogue du panneau d’informations dans l’arrière-plan du panneau de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p>Position verticale de la boîte de dialogue du panneau d’informations dans la zone de visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge gauche </span> </p> </td> 
   <td colname="col2"> <p>La marge gauche de la boîte de dialogue du panneau d’informations peut être utilisée à des fins de centrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge haut </span> </p> </td> 
   <td colname="col2"> <p>La marge supérieure de la boîte de dialogue du panneau d’informations peut être utilisée à des fins de centrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Remplissage de la boîte de dialogue interne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rayon de bordure </span> </p> </td> 
   <td colname="col2"> <p>Rayon de bordure de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ombre-boîte </span> </p> </td> 
   <td colname="col2"> <p>Ombre de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez une boîte de dialogue de panneau d’informations de 300 x 200 pixels centrée sur la zone de la visionneuse ; A un remplissage de 40 pixels en haut et un remplissage de 10 pixels sur tous les autres côtés, un arrière-plan gris clair et un rayon de bordure et une ombre portée de 10 pixels.

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

La boîte de dialogue Panneau d’informations a un bouton Fermer, et cliquez ou appuyez sur le bouton ferme la boîte de dialogue.

L’aspect de ce bouton est contrôlé par le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du bord droit de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du bord gauche de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état donné du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , que vous pouvez utiliser pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

Exemple - pour configurer un bouton de fermeture de boîte de dialogue de 28 x 28 pixels, positionné à 5 pixels du bord supérieur et droit de la boîte de dialogue du panneau d’informations, et affiche une image différente pour chacun des quatre états de bouton différents.

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
