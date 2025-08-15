---
title: Incorporer le partage
description: L’outil Incorporer le partage se compose d’un bouton ajouté au panneau Partage sur les réseaux sociaux et à la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil de partage sur les réseaux sociaux.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 08ba7a29-8b17-4167-a9f3-82aa4cf65556
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '2631'
ht-degree: 0%

---

# Incorporer le partage{#embed-share}

L’outil Incorporer le partage se compose d’un bouton ajouté au panneau Partage sur les réseaux sociaux et à la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil de partage sur les réseaux sociaux.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect du bouton de partage intégré est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embedshare
```

**Propriétés CSS de l’outil de partage intégré**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau Partage sur les réseaux sociaux en définissant `display:none` propriété CSS sur sa classe CSS.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) pour plus d’informations.

**Exemple** - Pour configurer un bouton de partage intégré de 28 x 28 pixels qui affiche une image différente pour chacun des quatre états de bouton différents :

```
.s7video360viewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7video360viewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7video360viewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7video360viewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

Le recouvrement d’arrière-plan qui couvre la page web lorsque la boîte de dialogue est active est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7backoverlay
```

**Propriétés CSS du recouvrement d’arrière-plan**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> d’opacité </span> </p> </td> 
   <td colname="col2"> <p>Opacité de la superposition en arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur de recouvrement de l’arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer une superposition d’arrière-plan en gris avec une opacité de 70 % :

```
.s7video360viewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Par défaut, la boîte de dialogue modale s’affiche centrée sur l’écran sur les ordinateurs de bureau et occupe toute la zone de la page web sur les appareils tactiles. Dans tous les cas, le positionnement et le dimensionnement de la boîte de dialogue sont gérés par le composant . La boîte de dialogue est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialog
```

**Propriétés CSS de la boîte de dialogue**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de rayon de bordure </span> </p> </td> 
   <td colname="col2"> <p> Rayon de la bordure de la boîte de dialogue, au cas où la boîte de dialogue ne prendrait pas le navigateur entier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d'arrière-plan de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Doit être désactivé ou défini sur 100 %, auquel cas la boîte de dialogue occupe toute la fenêtre du navigateur (ce mode est préférable sur les appareils tactiles). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Doit être désactivé ou défini sur 100 %, auquel cas la boîte de dialogue occupe toute la fenêtre du navigateur (ce mode est préférable sur les appareils tactiles). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer la boîte de dialogue afin qu’elle utilise toute la fenêtre du navigateur et présente un arrière-plan blanc sur les appareils tactiles :

```
.s7video360viewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L’en-tête de boîte de dialogue se compose d’une icône, d’un texte de titre et d’un bouton Fermer. Le conteneur d’en-tête est contrôlé avec .

```
.s7video360viewer .s7embeddialog .s7dialogheader
```

**Propriétés CSS de l’en-tête de boîte de dialogue**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure pour le contenu de l’en-tête. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icône et le texte du titre sont enveloppés dans un conteneur supplémentaire contrôlé par les éléments suivants :

```
.s7video360viewer .s7embeddialog .s7dialogheader .s7dialogline
```

**Propriétés CSS de la ligne de boîte de dialogue**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure de l’icône et du titre de l’en-tête </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icône d’en-tête est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogheadericon
```

**Propriétés CSS de l’icône d’en-tête de boîte de dialogue**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Image de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le titre de l’en-tête est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogheadertext
```

**Propriétés CSS du texte de l’en-tête de boîte de dialogue**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> d’épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Épaisseur de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de taille de police </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> famille de polices </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de texte interne. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton Fermer est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7closebutton
```

Propriétés **CSS de l’** du bouton Fermer

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Position verticale du bouton par rapport au conteneur d’en-tête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale du bouton par rapport au conteneur d’en-tête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Image du bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) pour plus d’informations.

**Exemple** - Pour configurer un en-tête de boîte de dialogue avec marge intérieure, icône de 24 x 14 pixels et titre en gras de 16 points. Enfin, un bouton Fermer de 28 x 28 pixels, positionné à deux pixels du haut et à deux pixels de la droite du conteneur de boîte de dialogue :

```
.s7video360viewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Le pied de boîte de dialogue se compose du bouton « Annuler ». Le conteneur de pied de page est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogfooter
```

**Propriétés CSS du &#x200B;** de pied de boîte de dialogue

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de bordure </span> </p> </td> 
   <td colname="col2"> <p> Bordure permettant de séparer visuellement le pied de page du reste de la boîte de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le pied de page comporte un conteneur interne qui conserve le bouton. Il est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogbuttoncontainer
```

**Propriétés CSS du conteneur de boutons de boîte de dialogue**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre le pied de page et le bouton. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton Tout sélectionner est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogactionbutton
```

Ce bouton n&#39;est disponible que sur les ordinateurs de bureau.

**Propriétés CSS du bouton Tout sélectionner**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte des boutons pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan des boutons pour chaque état. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le bouton Tout sélectionner prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Le bouton Annuler est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogcancelbutton
```

**Propriétés CSS du bouton Annuler de la boîte de dialogue**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte des boutons pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan des boutons pour chaque état. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

En outre, les deux boutons partagent une classe CSS commune qui peut contenir des paramètres CSS identiques pour les autres boutons de boîte de dialogue :

```
.s7video360viewer .s7embeddialog .s7dialogfooter .s7button
```

**Propriétés CSS du bouton**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> d’épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Épaisseur de police du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> famille de polices </p> </td> 
   <td colname="col2"> <p>Famille de polices des boutons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur de ligne </span> </p> </td> 
   <td colname="col2"> <p> Hauteur du texte dans le bouton. Affecte l’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> d'ombre </span> </p> </td> 
   <td colname="col2"> <p>Ombre portée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> de la marge droite </p> </td> 
   <td colname="col2"> <p>Marge du bouton droit. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) pour plus d’informations.

**Exemple** - pour configurer un pied de boîte de dialogue avec un bouton Annuler de 64 x 34, dont la couleur du texte et la couleur d’arrière-plan sont différentes pour chaque état de bouton :

```
.s7video360viewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
```

La zone de dialogue principale, entre l’en-tête et le pied de page, contient du contenu de boîte de dialogue défilable et un panneau de défilement à droite. Dans tous les cas, le composant gère la largeur de cette zone. Il n’est pas possible de la définir dans CSS. La zone de dialogue principale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogviewarea
```

**Propriétés CSS de la zone d’affichage de la boîte de dialogue**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de la zone de la boîte de dialogue principale. Elle ne doit être spécifiée que lorsque la boîte de dialogue fonctionne en mode bureau. Elle ne s’applique pas lorsque la boîte de dialogue est dimensionnée pour occuper toute la fenêtre du navigateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la zone de la boîte de dialogue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de la marge </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer une zone de boîte de dialogue principale pour qu’elle ait une hauteur de 300 pixels, une marge de dix pixels et un arrière-plan blanc :

```
.s7video360viewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Tout le contenu du formulaire (comme les libellés et les champs de saisie) réside dans un conteneur contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogbody
```

Si la hauteur de ce conteneur semble supérieure à celle de la zone de boîte de dialogue principale, un défilement vertical est automatiquement activé par le composant.

Propriétés **CSS du corps de la boîte de dialogue**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer le contenu d’un formulaire avec une marge intérieure de dix pixels :

```
.s7video360viewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Tous les libellés statiques du formulaire de boîte de dialogue sont contrôlés par

```
.s7video360viewer .s7embeddialog .s7dialoglabel
```

Cette classe ne convient pas pour contrôler la taille ou la position des libellés, car vous pouvez l’appliquer à des textes à différents endroits de l’interface utilisateur du formulaire.

**Propriétés CSS du libellé de la boîte de dialogue. &#x200B;**

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> d’épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Épaisseur de police des libellés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police des libellés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> famille de polices </p> </td> 
   <td colname="col2"> <p>Famille de polices des libellés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte du libellé. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les libellés des boîtes de dialogue peuvent être localisés. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) pour plus d’informations.

**Exemple** - pour configurer tous les libellés sur gris, en gras avec une police de neuf pixels :

```
.s7video360viewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

La taille de la copie de texte affichée au-dessus du code incorporé est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialoginputwide
```

**Propriétés CSS du champ de saisie de la boîte de dialogue**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du champ de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour définir la copie de texte sur une largeur de 430 pixels et une marge intérieure de dix pixels en bas :

```
.s7video360viewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Le code incorporé est encapsulé dans un conteneur et contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer
```

**Propriétés CSS du conteneur d’entrée de boîte de dialogue**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du conteneur de code incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure autour du conteneur de code incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour définir une bordure grise d’un pixel autour du texte du code incorporé, faites-en une largeur de 430 pixels et disposez d’une marge intérieure de dix pixels :

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

Le texte du code incorporé est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer
```

**Propriétés CSS du conteneur d’entrée de boîte de dialogue**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> un </span> de retour à la ligne </p> </td> 
   <td colname="col2"> <p>Style d'habillage Word. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer le code incorporé afin d’utiliser `break-word` habillage de mots :

```
.s7video360viewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Le libellé Taille d’incorporation et la liste déroulante se trouvent au bas de la boîte de dialogue et sont placés dans un conteneur contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel
```

**Propriétés CSS du panneau Taille d’incorporation de la boîte de dialogue**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer un panneau de taille incorporée avec une marge intérieure de dix pixels :

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

La taille et l’alignement de l’étiquette de taille d’incorporation sont contrôlés avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel
```

**Propriétés CSS du panneau Taille d’incorporation de la boîte de dialogue**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> un </span> d’alignement vertical </p> </td> 
   <td colname="col2"> <p>Alignement vertical des libellés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du libellé. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour définir le libellé de la taille d’incorporation sur aligné en haut et sur une largeur de 80 pixels :

```
.s7video360viewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

La largeur de la zone de liste déroulante de taille d’incorporation est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7combobox
```

**Propriétés CSS de la zone de liste modifiable**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la zone de liste déroulante. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La zone de liste modifiable prend en charge le sélecteur d’attributs `expanded` avec les valeurs possibles de `true` et `false`. La valeur `true` est utilisée lorsque la zone de liste modifiable affiche l’une des tailles d’incorporation prédéfinies ; elle doit donc prendre toute la largeur disponible. La valeur `false` est utilisée lorsque l’option Taille personnalisée est sélectionnée dans la zone de liste. Elle doit donc rétrécir pour laisser de l’espace aux champs de saisie de largeur et de hauteur personnalisés.

**Exemple** - pour définir la zone de liste de taille incorporée sur une largeur de 300 pixels lors de l’affichage d’un élément prédéfini et de 110 pixels lors de l’affichage d’une taille personnalisée :

```
.s7video360viewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7video360viewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

La hauteur du texte de la zone de liste modifiable est définie par un élément interne spécial et est contrôlée par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxtext
```

**Propriétés CSS du texte de la zone de liste modifiable**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du texte de la zone de liste déroulante. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour définir la hauteur de texte de la zone de liste de taille d’incorporation sur 40 pixels :

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

La zone de liste modifiable comporte un bouton « liste déroulante » à droite et elle est contrôlée par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**Propriétés CSS du bouton de zone de liste modifiable**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position verticale du bouton dans la zone de liste déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p>Position horizontale du bouton dans la zone de liste déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Image du bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

**Exemple** - pour définir un bouton déroulant sur 28 x 28 pixels et disposer d’une image distincte pour chaque état :

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Le panneau avec la liste des tailles d’incorporation affichée lorsque la zone de liste est ouverte est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7comboboxdropdown
```

La taille et la position du panneau sont contrôlées par le composant . Il n’est pas possible de le modifier via CSS.

**Propriétés CSS de la liste déroulante de zone de liste déroulante**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour définir le panneau de la zone de liste déroulante sur une bordure grise d’un pixel :

```
.s7video360viewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Un seul élément dans un panneau déroulant contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dropdownitemanchor
```

**Propriétés CSS de l’ancre d’élément de la liste déroulante**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Arrière-plan de l’élément. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour définir l’élément du panneau de la zone de liste comme ayant un arrière-plan blanc :

```
.s7video360viewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Une coche affichée à gauche de l’élément sélectionné dans le panneau de zone de liste modifiable contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7checkmark
```

**Propriétés CSS de la case à cocher**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Image de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour définir l’icône de coche sur 25 x 25 pixels :

```
.s7video360viewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Lorsque l’option « Taille personnalisée » est sélectionnée dans la zone de liste taille d’incorporation, la boîte de dialogue affiche deux champs de saisie supplémentaires à droite pour permettre à l’utilisateur de saisir une taille d’incorporation personnalisée. Ces champs sont placés dans un conteneur contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogcustomsizepanel
```

**Propriétés CSS du panneau Taille personnalisée de la boîte de dialogue**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p> Distance par rapport à la zone de liste de taille incorporée. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour définir la taille personnalisée du panneau des champs de saisie sur 20 pixels à droite de la zone de liste modifiable :

```
.s7video360viewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Chaque champ d’entrée de taille personnalisée est encapsulé dans un conteneur qui effectue le rendu d’une bordure et définit la marge entre les champs. Il est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogcustomsize
```

**Propriétés CSS de la taille personnalisée de la boîte de dialogue**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure autour du champ de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du champ de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de la marge </span> </p> </td> 
   <td colname="col2"> <p> Marge du champ de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure du champ de saisie. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour définir les champs de saisie de taille personnalisée sur une bordure grise d’un pixel, une marge, un remplissage et une largeur de 70 pixels :

```
.s7video360viewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Si un défilement vertical est nécessaire, la barre de défilement est rendue dans le panneau près du bord droit de la boîte de dialogue, qui est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7dialogscrollpanel
```

**Propriétés CSS du panneau de défilement de la boîte de dialogue**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du panneau de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer un panneau de défilement d’une largeur de 44 pixels

```
.s7video360viewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

L’aspect de la zone de la barre de défilement est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7scrollbar
```

**Propriétés CSS de la barre de défilement**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la barre de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Décalage de la barre de défilement verticale par rapport au haut du panneau de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inférieur </span> </p> </td> 
   <td colname="col2"> <p> La barre de défilement verticale est décalée par rapport au bas du panneau de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p> Décalage de la barre de défilement horizontale par rapport au bord droit du panneau de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer une barre de défilement de 28 pixels de large avec une marge de huit pixels en haut, à droite et en bas du panneau de défilement :

```
.s7video360viewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

La piste de la barre de défilement est la zone située entre les boutons de défilement supérieur et inférieur. Le composant définit automatiquement la position et la hauteur de la piste. La piste est contrôlée avec le sélecteur de classe CSS suivant

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**Propriétés CSS de la barre de défilement**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Suivre la couleur d’arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer une piste de barre de défilement de 28 pixels de large sur un arrière-plan gris :

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Le curseur de la barre de défilement se déplace verticalement dans une zone de piste de défilement. Sa position verticale est entièrement contrôlée par la logique du composant. Cependant, la hauteur du pouce ne change pas dynamiquement en fonction de la quantité de contenu. La hauteur du pouce et d’autres aspects peuvent être configurés avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**Propriétés CSS du curseur de la barre de défilement**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de remplissage supérieur </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure verticale entre le haut de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure verticale entre le bas de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de pouce donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de pouce : `up`, `down`, `over` et `disabled`.

**Exemple** - pour configurer une barre de défilement de 28 x 45 pixels, avec une marge de dix pixels en haut et en bas et une illustration différente pour chaque état :

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

L’aspect des boutons de défilement supérieur et inférieur est contrôlé avec les sélecteurs de classe CSS suivants :

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Il n’est pas possible de positionner des boutons de défilement à l’aide des propriétés CSS `top`, `left`, `bottom` et `right`. À la place, la logique de la visionneuse les positionne automatiquement.

**Propriétés CSS des boutons de défilement supérieur et inférieur**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ces boutons prennent en charge le sélecteur d’attributs de `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton : `up`, `down`, `over` et `disabled`.

Les info-bulles des boutons peuvent être localisées. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) pour plus d’informations.

**Exemple** - pour configurer des boutons de défilement de 28 x 32 pixels avec une illustration différente pour chaque état :

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
