---
description: L’outil de partage de liens est constitué d’un bouton ajouté au panneau de partage Social et de la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil de partage Social.
solution: Experience Manager
title: Partage de liens
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: 9eb2ef38-9b86-4c60-90a2-6609cb3fcc39
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1393'
ht-degree: 2%

---

# Partage de lien{#link-share}

L’outil de partage de liens est constitué d’un bouton ajouté au panneau de partage Social et de la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil de partage Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L’aspect du bouton de partage de liens est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkshare
```

**Propriétés CSS de l&#39;outil de partage de liens**

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
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau de partage Social en définissant la propriété `display:none` CSS sur sa classe CSS.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Exemple : pour configurer un bouton de partage de liens de 28 x 28 pixels et afficher une image différente pour chacun des quatre états de bouton différents :

```
.s7video360viewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7video360viewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7video360viewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7video360viewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

L’incrustation d’arrière-plan qui couvre la page Web lorsque la boîte de dialogue est principale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7backoverlay
```

**Propriétés CSS de l’incrustation d’arrière-plan**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité  </span> </p> </td> 
   <td colname="col2"> <p>Opacité de l’incrustation en arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’incrustation d’arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**  : pour configurer une incrustation d’arrière-plan en gris avec une opacité de 70 % :

```
.s7video360viewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Par défaut, la boîte de dialogue modale s’affiche au centre de l’écran sur les systèmes de bureau et occupe l’intégralité de la zone de page Web sur les périphériques tactiles. Dans tous les cas, le positionnement et le dimensionnement de la boîte de dialogue sont gérés par le composant. La boîte de dialogue est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialog
```

**Propriétés CSS de la boîte de dialogue**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Rayon de bordure de la boîte de dialogue, au cas où la boîte de dialogue ne prendrait pas la totalité du navigateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Doit être désactivée ou définie à 100 %, auquel cas la boîte de dialogue prend la totalité de la fenêtre du navigateur (ce mode est préférable sur les périphériques tactiles). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Doit être désactivée ou définie à 100 %, auquel cas la boîte de dialogue prend la totalité de la fenêtre du navigateur (ce mode est préférable sur les périphériques tactiles). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer la boîte de dialogue afin d’utiliser la fenêtre entière du navigateur et d’avoir un arrière-plan blanc sur les périphériques tactiles :

```
.s7video360viewer.s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L’en-tête de la boîte de dialogue se compose d’une icône, d’un texte de titre et d’un bouton de fermeture. Le conteneur d’en-tête est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialogheader
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

L’icône et le texte du titre sont encapsulés dans un conteneur supplémentaire contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline
```

**Propriétés CSS de la ligne de dialogue**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure de l’icône d’en-tête et du titre </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;icône d&#39;en-tête est contrôlée avec le sélecteur de classe CSS suivant

```
.s7video360viewer .s7linkdialog .s7dialogheadericon
```

**Propriétés CSS de l’icône d’en-tête de la boîte de dialogue**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Image d’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le titre d’en-tête est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialogheadertext
```

**Propriétés CSS du texte d’en-tête de la boîte de dialogue**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-poids  </span> </p> </td> 
   <td colname="col2"> <p>Poids des polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure du texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton Fermer est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7closebutton
```

**Propriétés CSS du bouton de fermeture **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p> Position verticale du bouton par rapport au conteneur d’en-tête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale du bouton par rapport au conteneur d’en-tête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Image de bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton Fermer et le titre de la boîte de dialogue peuvent être localisés. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Exemple**  : pour configurer un en-tête de boîte de dialogue avec remplissage, une icône de 22 x 12 pixels, un titre en gras de 16 points et un bouton de fermeture de 28 x 28 pixels placé deux pixels du haut et deux pixels de droite du conteneur de la boîte de dialogue :

```
.s7video360viewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Le pied de page de la boîte de dialogue se compose d’un bouton Annuler. Le conteneur de pied de page est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialogfooter
```

**Propriétés CSS du pied de page de la boîte de dialogue **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p> Bordure que vous pouvez utiliser pour séparer visuellement le pied de page du reste de la boîte de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le pied de page comporte un conteneur interne qui conserve le bouton. Il est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer
```

**Propriétés CSS du conteneur de bouton de la boîte de dialogue**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre le pied de page et le bouton. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton Sélectionner tout est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialogactionbutton
```

Le bouton est disponible uniquement sur les systèmes de bureau.

**Propriétés CSS du bouton Sélectionner tout**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte des boutons pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du bouton pour chaque état. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le bouton Sélectionner tout prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Le bouton Annuler est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialogcancelbutton
```

**Propriétés CSS du bouton Annuler de la boîte de dialogue**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte des boutons pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du bouton pour chaque état. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

En outre, les deux boutons partagent la même classe CSS commune qui peut contenir des paramètres CSS identiques pour les autres boutons de boîte de dialogue :

```
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button
```

**Propriétés CSS du bouton**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-poids  </span> </p> </td> 
   <td colname="col2"> <p>Poids de police de bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police des boutons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices de bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ligne-hauteur  </span> </p> </td> 
   <td colname="col2"> <p> Hauteur du texte à l’intérieur du bouton. Affecte l’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow  </span> </p> </td> 
   <td colname="col2"> <p>Déposez l'ombre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge droite  </span> </p> </td> 
   <td colname="col2"> <p>Marge du bouton droit. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les info-bulles des boutons peuvent être localisées. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Exemple**  : pour configurer un pied de page de boîte de dialogue avec un bouton Annuler de 64 x 34, avec des couleurs de texte et d’arrière-plan différentes pour chaque état de bouton :

```
.s7video360viewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

La zone de dialogue principale (entre l’en-tête et le pied de page) contient le contenu de la boîte de dialogue. Dans tous les cas, le composant gère la largeur de cette zone ; il n’est pas possible de la définir dans CSS. La zone de dialogue principale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialogviewarea
```

**Propriétés CSS de la zone d’affichage de la boîte de dialogue **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de la zone de boîte de dialogue principale. Elle ne doit être spécifiée que lorsque la boîte de dialogue fonctionne en mode Bureau. Il n’est pas applicable lorsque la boîte de dialogue est dimensionnée pour occuper l’intégralité de la fenêtre du navigateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la zone de boîte de dialogue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**  : pour configurer une zone de boîte de dialogue principale de 300 pixels de hauteur, d’une marge de 10 pixels et d’un arrière-plan blanc :

```
.s7video360viewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Tout le contenu du formulaire, tel que les libellés et les champs d’entrée, réside dans un conteneur contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialogbody
```

**Propriétés CSS du corps de la boîte de dialogue **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - pour configurer le contenu du formulaire avec un remplissage de 10 pixels :

```
.s7interactivevideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

Tous les libellés statiques du formulaire de boîte de dialogue sont contrôlés avec

```
.s7video360viewer .s7linkdialog .s7dialoglabel
```

Cette classe n’est pas adaptée au contrôle de la taille ou de la position de l’étiquette, car vous pouvez l’appliquer à des textes situés à divers endroits de l’interface utilisateur du formulaire.

**Propriétés CSS du libellé de la boîte de dialogue. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-poids  </span> </p> </td> 
   <td colname="col2"> <p>Poids de police d’étiquette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police du libellé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Libeller la famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte du libellé. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les libellés de la boîte de dialogue peuvent être localisés. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Exemple**  : pour définir toutes les étiquettes en gris, en gras avec une police de neuf pixels :

```
.s7video360viewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

La taille de la copie de texte affichée au-dessus du lien est contrôlée par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialoginputwide
```

**Propriétés CSS du champ large d’entrée de la boîte de dialogue**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**  : pour définir la copie de texte sur 430 pixels de large et un remplissage de 10 pixels en bas :

```
.s7video360viewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Le lien de partage est encapsulé dans un conteneur et contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer
```

**Propriétés CSS du conteneur d’entrée de la boîte de dialogue**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure autour du conteneur de lien de partage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**  : pour définir une bordure grise d’un pixel autour du texte du code incorporé et disposer de neuf pixels de remplissage :

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

Le lien de partage lui-même est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7linkdialog .s7dialoglink
```

**Propriétés CSS du lien de partage de la boîte de dialogue**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Partager la largeur du lien. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**  : pour définir le lien de partage sur 450 pixels de large :

```
.s7video360viewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```
