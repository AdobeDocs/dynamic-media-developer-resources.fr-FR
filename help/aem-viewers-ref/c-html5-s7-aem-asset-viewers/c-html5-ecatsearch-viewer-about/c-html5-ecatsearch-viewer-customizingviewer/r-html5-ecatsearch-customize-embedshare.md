---
title: Incorporer le partage
description: L’outil de partage intégré est constitué d’un bouton ajouté au panneau Partage sur les réseaux sociaux et de la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil Partage sur les réseaux sociaux .
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 82117b6e-c0be-4538-90ab-8def7521b49c
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '2606'
ht-degree: 2%

---

# Incorporer le partage{#embed-share}

L’outil de partage intégré est constitué d’un bouton ajouté au panneau Partage sur les réseaux sociaux et de la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil Partage sur les réseaux sociaux .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect du bouton d’intégration du partage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embedshare
```

**Propriétés CSS de l’outil de partage intégré**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge `state` sélecteur d’attributs qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau Partage sur les réseaux sociaux en définissant `display:none` Propriété CSS sur sa classe CSS.

L’info-bulle de bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un bouton de partage incorporé de 28 x 28 pixels et afficher une image différente pour chacun des quatre états de bouton différents :

```
.s7ecatalogsearchviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

La superposition en arrière-plan qui couvre la page web lorsque la boîte de dialogue est principale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay
```

**Propriétés CSS de la superposition en arrière-plan**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p>Opacité de la superposition en arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de superposition de l’arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une superposition en arrière-plan de sorte qu’elle soit grise avec une opacité de 70 % :

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Par défaut, la boîte de dialogue modale s’affiche centrée dans l’écran sur les systèmes de bureau et occupe l’ensemble de la zone de page web sur les appareils tactiles. Dans tous les cas, le positionnement et le dimensionnement de la boîte de dialogue sont gérés par le composant. La boîte de dialogue est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialog
```

**Propriétés CSS de la boîte de dialogue**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Rayon de bordure de la boîte de dialogue, au cas où la boîte de dialogue ne prendrait pas l’intégralité du navigateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>doit être désactivée ou définie sur 100 %, auquel cas la boîte de dialogue s’ouvre sur l’ensemble de la fenêtre du navigateur (ce mode est préférable sur les appareils tactiles). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>doit être désactivée ou définie sur 100 %, auquel cas la boîte de dialogue s’ouvre sur l’ensemble de la fenêtre du navigateur (ce mode est préférable sur les appareils tactiles). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer la boîte de dialogue afin d’utiliser toute la fenêtre du navigateur et d’avoir un arrière-plan blanc sur les appareils tactiles :

```
.s7ecatalogsearchviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L’en-tête de la boîte de dialogue se compose d’une icône, d’un texte de titre et d’un bouton de fermeture. Le conteneur d’en-tête est contrôlé avec

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader
```

**Propriétés CSS de l’en-tête de la boîte de dialogue**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure du contenu de l’en-tête. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icône et le texte du titre sont placés dans un conteneur supplémentaire contrôlé par

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**Propriétés CSS de la ligne de boîte de dialogue**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure de l’icône et du titre de l’en-tête </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icône d’en-tête est contrôlée avec le sélecteur de classe CSS suivant

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon
```

**Propriétés CSS de l’icône d’en-tête de la boîte de dialogue**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Image de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le titre d’en-tête est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext
```

**Propriétés CSS du texte de l’en-tête de la boîte de dialogue**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Poids de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure du texte interne. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton Fermer est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton
```

Propriétés **CSS du bouton de fermeture **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p> Position verticale des boutons par rapport au conteneur d’en-tête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p> Position du bouton horizontal par rapport au conteneur d’en-tête. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Image de bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge `state` sélecteur d’attributs qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle de bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un en-tête de boîte de dialogue avec marge intérieure, une icône de 24 x 14 pixels et un titre de 16 points en gras. Enfin, un bouton Fermer de 28 x 28 pixels, positionné deux pixels du haut, et deux pixels à droite du conteneur de la boîte de dialogue :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Le pied de page de la boîte de dialogue se compose du bouton &quot;Annuler&quot;. Le conteneur de pied de page est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter
```

Propriétés **CSS du pied de page de la boîte de dialogue **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p> Bordure que vous pouvez utiliser pour séparer visuellement le pied de page du reste de la boîte de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le pied de page comporte un conteneur interne qui conserve le bouton. Il est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer
```

**Propriétés CSS du conteneur de boutons de la boîte de dialogue**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre le pied de page et le bouton. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton Tout sélectionner est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton
```

Ce bouton n’est disponible que sur les ordinateurs de bureau.

**Propriétés CSS du bouton Tout sélectionner**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Couleur de texte des boutons pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du bouton pour chaque état. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le bouton Tout sélectionner prend en charge la variable `state` sélecteur d’attributs qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Le bouton Annuler est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton
```

**Propriétés CSS du bouton d’annulation de la boîte de dialogue**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Couleur de texte des boutons pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du bouton pour chaque état. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge `state` sélecteur d’attributs qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

En outre, les deux boutons partagent une classe CSS commune, qui peut contenir des paramètres CSS identiques pour les autres boutons de boîte de dialogue :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button
```

**Propriétés CSS du bouton**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Poids de police du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices de bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Hauteur du texte dans le bouton. Affecte l’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Abandonner l'ombre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>Marge du bouton droit. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle de bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un pied de page de boîte de dialogue avec un bouton Annuler 64 x 34, un bouton Tout sélectionner 82 x 34, avec une couleur de texte et une couleur d’arrière-plan différentes pour chaque état de bouton :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

La zone de dialogue principale (entre l’en-tête et le pied de page) contient le contenu de la boîte de dialogue défilante et le panneau de défilement à droite. Dans tous les cas, le composant gère la largeur de cette zone. Il n’est pas possible de la définir dans CSS. La zone de boîte de dialogue principale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea
```

Propriétés **CSS de la zone d’affichage de la boîte de dialogue **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de la zone de boîte de dialogue principale. Elle doit être spécifiée uniquement lorsque la boîte de dialogue fonctionne en mode bureau. Cela ne s’applique pas lorsque la boîte de dialogue est dimensionnée pour occuper toute la fenêtre du navigateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la zone de boîte de dialogue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une zone de boîte de dialogue principale d’une hauteur de 300 pixels, définissez une marge de dix pixels et utilisez un arrière-plan blanc :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Tout le contenu du formulaire (comme les libellés et les champs de saisie) se trouve dans un conteneur contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody
```

Si la hauteur de ce conteneur semble supérieure à la zone de boîte de dialogue principale, un défilement vertical est activé automatiquement par le composant.

Propriétés **CSS du corps de la boîte de dialogue **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer le contenu d’un formulaire avec une marge intérieure de dix pixels :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Tous les libellés statiques du formulaire de boîte de dialogue sont contrôlés par

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel
```

Cette classe ne convient pas au contrôle de la taille ou de la position des libellés, car vous pouvez l’appliquer à des textes situés à différents endroits de l’interface utilisateur du formulaire.

Propriétés **CSS du libellé de la boîte de dialogue. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Etiqueter le poids de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Étiqueter la taille de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Étiqueter la famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte du libellé. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les libellés des boîtes de dialogue peuvent être localisés. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer toutes les étiquettes en gris, en gras avec une police de neuf pixels :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

La taille de la copie de texte affichée en haut du code incorporé est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide
```

**Propriétés CSS du champ d’entrée de la boîte de dialogue**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du champ de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir une copie de texte de 430 pixels de large et une marge intérieure de dix pixels en bas :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Le code incorporé est encapsulé dans un conteneur et contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**Propriétés CSS du conteneur d’entrée de la boîte de dialogue**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du conteneur de code incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure autour du conteneur de code incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir une bordure grise d’un pixel autour du texte du code incorporé, faites-la 430 pixels de large et ajoutez une marge intérieure de dix pixels :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

Le texte du code incorporé réel est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**Propriétés CSS du conteneur d’entrée de la boîte de dialogue**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap </span> </p> </td> 
   <td colname="col2"> <p>Style d’encapsulation de mot. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer le code incorporé à utiliser `break-word` retour à la ligne :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Le libellé de taille d’incorporation et la liste déroulante se trouvent au bas de la boîte de dialogue et sont placés dans un conteneur contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**Propriétés CSS du panneau Taille de la boîte de dialogue**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un panneau de taille d’incorporation afin qu’il ait dix pixels de remplissage :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

La taille et l’alignement du libellé de taille d’intégration sont contrôlés avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**Propriétés CSS du panneau Taille de la boîte de dialogue**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement vertical </span> </p> </td> 
   <td colname="col2"> <p>Alignement vertical des libellés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du libellé. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir le libellé de la taille d’intégration de sorte qu’il soit aligné en haut et de 80 pixels de large :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

La largeur de la zone combinée de taille d’intégration est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox
```

**Propriétés CSS de la zone de liste modifiable**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la zone de liste déroulante. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La zone de liste modifiable prend en charge la variable `expanded` sélecteur d’attributs avec les valeurs possibles de `true` et `false`. La valeur `true` est utilisée lorsque la zone de liste modifiable affiche l’une des tailles incorporées prédéfinies. Elle doit donc prendre toute la largeur disponible. La valeur `false` est utilisée lorsque l’option de taille personnalisée est sélectionnée dans la zone combinée. Elle doit donc être réduite pour libérer de l’espace pour les champs de saisie de largeur et de hauteur personnalisés.

Exemple : pour définir la zone combinée de taille d’intégration sur 300 pixels de large lors de l’affichage d’un élément prédéfini et 110 pixels de large lors de l’affichage d’une taille personnalisée :

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

La hauteur du texte de zone combinée est définie par un élément interne spécial et est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**Propriétés CSS du texte de zone combinée**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du texte de la zone de liste déroulante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir la hauteur du texte de la zone combinée de taille d’intégration sur 40 pixels :

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

La zone de liste modifiable comporte un bouton &quot;déroulant&quot; à droite et elle est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**Propriétés CSS du bouton de zone combinée**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position du bouton vertical à l’intérieur de la zone combinée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p>Position du bouton horizontal à l’intérieur de la zone combinée. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Image de bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge `state` sélecteur d’attributs qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Exemple : pour définir un bouton déroulant sur 28 x 28 pixels et disposer d’une image distincte pour chaque état :

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Le panneau avec la liste des tailles d’intégration affichée à l’ouverture d’une zone de liste modifiable est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown
```

La taille et la position du panneau sont contrôlées par le composant. Il n’est pas possible de le modifier via CSS.

**Propriétés CSS de la liste déroulante de zone de liste modifiable**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir le panneau de zone combinée sur une bordure grise d’un pixel :

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Un seul élément d’un panneau déroulant contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor
```

**Propriétés CSS de l’ancre d’élément de liste déroulante**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Arrière-plan des éléments. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir l’élément de panneau de zone combinée sur un arrière-plan blanc :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Coche affichée à gauche de l’élément sélectionné dans le panneau de zone combinée contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark
```

**Propriétés CSS de la case à cocher**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Image de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir l’icône de coche sur 25 x 25 pixels :

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Lorsque l’option &quot;Taille personnalisée&quot; est sélectionnée dans la zone combinée Taille de l’intégration, la boîte de dialogue affiche deux champs de saisie supplémentaires à droite pour permettre à l’utilisateur de saisir une taille d’intégration personnalisée. Ces champs sont placés dans un conteneur contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel
```

**Propriétés CSS du panneau de taille personnalisée de la boîte de dialogue**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p> Distance par rapport à la zone combinée de taille d’intégration. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir la taille personnalisée du panneau des champs d’entrée sur 20 pixels à droite de la zone de liste modifiable :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Chaque champ d’entrée de taille personnalisée est encapsulé dans un conteneur qui effectue le rendu d’une bordure et définit la marge entre les champs. Il est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize
```

**Propriétés CSS de la boîte de dialogue, taille personnalisée**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure autour du champ de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du champ de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Marge du champ de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure des champs de saisie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir la taille personnalisée des champs de saisie sur une bordure grise d’un pixel, une marge, une marge intérieure et une largeur de 70 pixels :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Si un défilement vertical est nécessaire, la barre de défilement est rendue dans le panneau près du bord droit de la boîte de dialogue, qui est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel
```

**Propriétés CSS du panneau de défilement de la boîte de dialogue**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du panneau de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un panneau de défilement d’une largeur de 44 pixels

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

L’aspect de la zone de barre de défilement est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar
```

**Propriétés CSS de la barre de défilement**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la barre de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p> Décalage de la barre de défilement verticale à partir du haut du panneau de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p> Décalage de la barre de défilement verticale à partir du bas du panneau de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p> Décalage de la barre de défilement horizontale à partir du bord droit du panneau de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une barre de défilement de 28 pixels de large et dont la marge de huit pixels se trouve en haut, à droite et au bas du panneau de défilement :

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Le suivi de la barre de défilement est la zone entre les boutons de défilement supérieur et inférieur. Le composant définit automatiquement la position et la hauteur du suivi. Le suivi est contrôlé à l’aide du sélecteur de classe CSS suivant

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**Propriétés CSS du suivi de la barre de défilement**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du suivi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Suivi de la couleur d’arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un suivi de barre de défilement de 28 pixels de large et avec un arrière-plan gris :

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

La barre de défilement se déplace verticalement dans une zone de suivi de défilement. Sa position verticale est entièrement contrôlée par la logique du composant. Toutefois, la hauteur de la miniature ne change pas dynamiquement en fonction de la quantité de contenu. La hauteur du pouce et d’autres aspects peuvent être configurés avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**Propriétés CSS de la barre de défilement**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage-top </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure verticale entre le haut de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage-bottom </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure verticale entre le bas de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de pouce donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le curseur prend en charge `state` le sélecteur d’attributs, qui peut être utilisé pour appliquer différents habillages à différents états de pouce : `up`, `down`, `over`, et `disabled`.

Exemple : pour configurer une barre de défilement de 28 x 45 pixels, avec une marge de dix pixels en haut et en bas et une illustration différente pour chaque état :

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

L’aspect des boutons de défilement haut et bas est contrôlé à l’aide des sélecteurs de classe CSS suivants :

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Il n’est pas possible de positionner des boutons de défilement à l’aide de CSS `top`, `left`, `bottom`, et `right` propriétés. À la place, la logique de la visionneuse les positionne automatiquement.

**Propriétés CSS des boutons de défilement haut et bas**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ces boutons prennent en charge la fonction `state` le sélecteur d’attributs, qui peut être utilisé pour appliquer différents habillages à différents états de bouton : `up`, `down`, `over`, et `disabled`.

Les info-bulles des boutons peuvent être localisées. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer des boutons de défilement de 28 x 32 pixels et dont l’illustration est différente pour chaque état :

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
