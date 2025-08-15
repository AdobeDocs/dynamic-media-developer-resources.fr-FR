---
title: Partage email
description: L’outil de partage de courrier électronique se compose d’un bouton ajouté au panneau de partage de Social et à la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil de partage Social.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f2685d59-6b92-49cf-9359-dda602af4297
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '3029'
ht-degree: 0%

---

# Partage email{#email-share}

L’outil de partage de courrier électronique se compose d’un bouton ajouté au panneau de partage de Social et à la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil de partage Social.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’apparence du bouton de partage de courrier électronique est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emailshare
```

**Propriétés CSS de l’outil de partage de courrier électronique.**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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
   <td colname="col2"> <p> Image affichée pour un état donné du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau de partage Social en définissant `display:none` la propriété CSS sur sa classe CSS.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple - pour configurer un bouton de partage de courrier électronique de 28 x 28 pixels et qui affiche une image différente pour chacun des quatre états différents du bouton.

```
.s7smartcropvideoviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

La superposition d’arrière-plan qui couvre une page Web lorsque la boîte de dialogue est active est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7backoverlay
```

**Propriétés CSS du recouvrement arrière**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p> Opacité de la superposition d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur de superposition d’arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour définir le recouvrement d’arrière-plan de manière à ce qu’il soit gris avec un taux d’opacité de 70 % :

```
.s7smartcropvideoviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Par défaut, la boîte de dialogue modale s’affiche centrée sur l’écran sur les ordinateurs de bureau et occupe toute la zone de la page Web sur les appareils tactiles. Dans tous les cas, le positionnement et le dimensionnement de la boîte de dialogue sont gérés par le composant. La boîte de dialogue est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialog
```

**Propriétés CSS de la boîte de dialogue**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rayon de bordure </span> </p> </td> 
   <td colname="col2"> <p> Rayon de bordure de la boîte de dialogue (dans le cas où la boîte de dialogue ne prend pas toute la fenêtre du navigateur) ; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan de la boîte de dialogue ; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Doit être soit non réglé, soit réglé sur 100 %, auquel cas la boîte de dialogue prend toute la fenêtre du navigateur (ce mode est préféré sur les appareils tactiles) ; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p> Doit être soit non défini, soit réglé sur 100 %, auquel cas la boîte de dialogue prend toute la fenêtre du navigateur (ce mode est préféré sur les appareils tactiles). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer la boîte de dialogue afin d’utiliser toute la fenêtre du navigateur et d’avoir un fond blanc sur les appareils tactiles :

```
.s7smartcropvideoviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L’en-tête de boîte de dialogue se compose d’une icône, d’un texte de titre et d’un bouton Fermer. Le conteneur d’en-tête est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader
```

**Propriétés CSS de l’en-tête de boîte de dialogue**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure du contenu d’en-tête. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icône et le texte du titre sont placés dans un conteneur supplémentaire contrôlé par

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**Propriétés CSS de la boîte de dialogue**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure de l’icône d’en-tête et du titre </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icône d’en-tête est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadericon
```

**Propriétés CSS de l’icône d’en-tête de boîte de dialogue**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Image de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le titre de l’en-tête est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadertext
```

**Propriétés CSS du texte d’en-tête de la boîte de dialogue**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Graisse de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Remplissage de texte interne. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton Fermer est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7closebutton
```

**Propriétés CSS du bouton de fermeture **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p> Position verticale du bouton par rapport au conteneur d’en-tête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Droite </span> </p> </td> 
   <td colname="col2"> <p> Position horizontale du bouton par rapport au conteneur d’en-tête. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Remplissage intérieur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Image de bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton Fermer et le titre de la boîte de dialogue peuvent être localisés. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple - Pour configurer un en-tête de boîte de dialogue avec une remplissage, une icône de 24 x 17 pixels et un titre en gras de 16 points. Enfin, un bouton Fermer de 28 x 28 pixels, positionné à deux pixels du haut et à deux pixels de la droite du conteneur de dialogue :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Le pied de page de boîte de dialogue se compose des boutons « annuler » et « envoyer un e-mail ». Le conteneur de pied de page est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter
```

**Propriétés CSS du pied de page de boîte de dialogue **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> frontière </span> </p> </td> 
   <td colname="col2"> <p> Bordure qui peut être utilisée pour séparer visuellement le pied de page du reste de la boîte de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le pied de page a un conteneur intérieur qui conserve les deux boutons. Elle est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbuttoncontainer
```

**Propriétés CSS du conteneur de boutons de la boîte de dialogue**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p> Remplissage intérieur entre le pied de page et les boutons. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton Annuler est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton
```

**Propriétés CSS du bouton Annuler de la boîte de dialogue**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte du bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan des boutons pour chaque état. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Le bouton Envoyer un courrier électronique est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton
```

**Propriétés CSS du bouton d’action de la boîte de dialogue**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte du bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan des boutons pour chaque état. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

En outre, les deux boutons partagent une classe CSS commune qui peut contenir des paramètres CSS identiques pour les autres boutons de boîte de dialogue :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter .s7button
```

**Propriétés CSS du bouton**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Graisse de police du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police des boutons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices des boutons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur de ligne </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de texte dans le bouton. Affecte l’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ombre-boîte </span> </p> </td> 
   <td colname="col2"> <p>Ombre portée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge droite </span> </p> </td> 
   <td colname="col2"> <p>Marge du bouton droit. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les info-bulles des boutons peuvent être localisées. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple - Pour configurer un pied de page de boîte de dialogue avec un bouton Annuler 64 x 34 et un bouton Envoyer un courrier électronique de 82 x 34. Enfin, la couleur du texte et la couleur d’arrière-plan sont différentes pour chaque état du bouton :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

La zone de dialogue principale, entre l’en-tête et le pied de page, contient le contenu de la boîte de dialogue défilante et le panneau de défilement sur la droite. Dans tous les cas, le composant gère la largeur de cette zone, il n’est pas possible de la définir dans CSS. La zone de dialogue principale est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea
```

**Propriétés CSS de la zone d’affichage de la boîte de dialogue **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de la zone principale de la boîte de dialogue. Il doit être spécifié uniquement lorsque la boîte de dialogue fonctionne en mode Bureau. Elle n’est pas applicable lorsque la boîte de dialogue est dimensionnée pour occuper toute la fenêtre du navigateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la boîte de dialogue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La boîte de dialogue principale prend en charge le sélecteur d’attributs facultatif `state` . Il est défini sur `sendsuccess` lorsque le formulaire de courrier électronique est envoyé et la boîte de dialogue affiche un message de confirmation. Tant que le message de confirmation est petit, ce sélecteur d’attributs peut être utilisé pour réduire la hauteur de la boîte de dialogue lorsque ce message de confirmation est affiché.

Exemple : pour définir la zone de la boîte de dialogue principale de manière à ce qu’elle ait initialement une hauteur de 300 pixels et une hauteur de 100 pixels lorsque le message de confirmation s’affiche, ayez une marge de dix pixels et utilisez un fond blanc :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

Tout le contenu du formulaire (tels que les libellés et les champs de saisie) réside dans un conteneur contrôlé par

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody
```

Si la hauteur de ce conteneur semble supérieure à la zone de boîte de dialogue principale, un défilement vertical est activé automatiquement par le composant.

**Propriétés CSS du corps de la boîte de dialogue **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Rembourrage intérieur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer le contenu d’un formulaire avec un remplissage de dix pixels :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

Le formulaire de boîte de dialogue est rempli ligne par ligne, chaque ligne portant une partie du contenu du formulaire (comme une étiquette et un champ de saisie de texte). La ligne de formulaire unique est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**Propriétés CSS de la ligne de boîte de dialogue**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Rembourrage de ligne intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer un formulaire de boîte de dialogue avec un remplissage de dix pixels pour chaque ligne :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Tous les libellés statiques du formulaire de boîte de dialogue sont contrôlés par

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoglabel
```

Cette classe ne convient pas au contrôle de la taille ou de la position des étiquettes, car vous pouvez l’appliquer à des textes situés à différents endroits de l’interface utilisateur du formulaire.

**Propriétés CSS du libellé de la boîte de dialogue. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Épaisseur de police de l’étiquette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police de l’étiquette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices d’étiquettes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte de l’étiquette. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les libellés de boîte de dialogue peuvent être localisés. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple : pour définir toutes les étiquettes de manière à ce qu’elles soient grises, en gras avec une police de neuf pixels :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Toutes les étiquettes statiques affichées à gauche des champs de saisie du formulaire sont contrôlées par :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputlabel
```

**Propriétés CSS de l’étiquette d’entrée de la boîte de dialogue**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du libellé statique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement de texte </span> </p> </td> 
   <td colname="col2"> <p>Alignement de texte horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Marge d’étiquette statique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Remplissage d’étiquette statique. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer des libellés de champ de saisie d’une largeur de 50 pixels, alignés à droite, avec une marge de remplissage de dix pixels et une marge de dix pixels sur la droite :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Chaque champ de saisie de formulaire est enveloppé dans le conteneur, ce qui vous permet d’appliquer une bordure personnalisée autour du champ de saisie. Elle est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer
```

**Propriétés CSS du conteneur d’entrée de la boîte de dialogue**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> frontière </span> </p> </td> 
   <td colname="col2"> <p>Bordure autour du conteneur de champs de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Rembourrage intérieur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le conteneur de champs de saisie prend en charge le sélecteur d’attributs facultatif `state` . Il est défini sur `verifyerror` lorsque l’utilisateur commet une erreur dans le format des données d’entrée et que la validation en ligne échoue. Ce sélecteur d’attributs permet de mettre en surbrillance une entrée utilisateur incorrecte dans le formulaire.

La plupart des champs de saisie qui s’étendent de l’étiquette sur la gauche jusqu’au bord droit du corps de la boîte de dialogue (qui comprend le champ « de » et le champ « message ») sont contrôlés par :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputwide
```

**Propriétés CSS du champ largeur d’entrée de la boîte de dialogue**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du champ d’entrée. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le champ de saisie « À » est plus étroit car il alloue de l’espace pour le bouton « Supprimer l’e-mail » à droite. Elle est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputshort
```

**Propriétés CSS de la boîte de dialogue Champ court d’entrée**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du champ d’entrée. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer un formulaire avec une bordure grise d’un pixel avec neuf pixels de remplissage autour de tous les champs de saisie. Pour avoir la même bordure de couleur rouge pour les champs qui échouent à la validation, pour avoir un champ de saisie « To » de 250 pixels de large, et le reste des champs de saisie 300 pixels de large :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

Le champ de saisie des messages électroniques est également contrôlé par :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogmessage
```

Cette classe permet de définir des propriétés spécifiques pour l’élément sous-jacent `TEXTAREA` .

**Propriétés CSS du message de boîte de dialogue**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> retour à la ligne automatique </span> </p> </td> 
   <td colname="col2"> <p>Style de renvoi à la ligne du mot. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un message électronique de 50 pixels de haut et utiliser le `break-word` retour automatique à la ligne :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

Le bouton « Ajouter une autre adresse e-mail » permet à un utilisateur d’ajouter plus d’un destinataire dans le formulaire de courrier électronique. Elle est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton
```

**Propriétés CSS de la boîte de dialogue Bouton Ajouter une adresse électronique**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte du bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Image de bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Position de l’image du bouton dans la zone du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Graisse de police du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police des boutons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices des boutons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur de ligne </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de texte dans le bouton. Modifie l’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement de texte </span> </p> </td> 
   <td colname="col2"> <p>Alignement de texte horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Rembourrage intérieur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple - pour définir le bouton « Ajouter une autre adresse e-mail » de 25 pixels de haut, utilisez une police en gras de 12 points avec alignement à droite et une couleur et une image de texte différentes pour chaque état :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

Le bouton « Supprimer » permet à un utilisateur de supprimer des destinataires supplémentaires du formulaire électronique. Elle est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton
```

**Propriétés CSS de la boîte de dialogue Supprimer le bouton de suppression de l’adresse électronique**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
 <tbody> 
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
   <td colname="col2"> <p>Image de bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple - pour configurer un bouton « Supprimer » de 25 x 25 pixels et utiliser une image différente pour chaque état :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

Le contenu partagé s’affiche au bas du corps de la boîte de dialogue et comprend une miniature, un titre, une URL d’origine et une description. Il est emballé dans un récipient contrôlé par :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**Propriétés CSS du contenu de la boîte de dialogue **

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> frontière </span> </p> </td> 
   <td colname="col2"> <p>Bordure de conteneur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Rembourrage intérieur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer un conteneur inférieur de sorte qu’il ait une bordure pointillée d’un pixel sans remplissage :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

L’image miniature est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogthumbnail
```

La `background-image` propriété est définie par la logique du composant.

**Propriétés CSS de l’image miniature de la boîte de dialogue**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement vertical </span> </p> </td> 
   <td colname="col2"> <p>Miniature d’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Rembourrage intérieur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer la miniature de 90 x 60 pixels et alignée en haut avec dix pixels de remplissage :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

Le titre, l’origine et la description du contenu sont ensuite regroupés dans un panneau à droite de la miniature du contenu. Elle est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginfopanel
```

**Propriétés CSS du panneau d’informations de la boîte de dialogue**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer un panneau d’informations sur le contenu de 300 pixels de large :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

Le titre du contenu est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogtitle
```

**Propriétés CSS du titre de la boîte de dialogue**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Graisse de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un titre de contenu de sorte qu’il utilise une police en gras et une marge de dix pixels :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

L’origine du contenu est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogorigin
```

**Propriétés CSS de l’origine du contenu de la boîte de dialogue **

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Graisse de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer l’origine du contenu de sorte qu’elle ait une marge de dix pixels :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

La description du contenu est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogdescription
```

**Propriétés CSS de la boîte de dialogue description du contenu**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Graisse de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir une description de contenu de manière à avoir une marge de dix pixels et utiliser une police de neuf points :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

Lorsqu’un utilisateur entre des données d’entrée incorrectes et que la validation en ligne échoue, ou lorsque la boîte de dialogue doit générer une erreur ou un message de confirmation lors de l’envoi du formulaire, un message s’affiche en haut du corps de la boîte de dialogue. Elle est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage
```

**Propriétés CSS de la boîte de dialogue message d’erreur**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Icône d’erreur. La valeur par défaut est un point d’exclamation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position de l’icône d’erreur dans la zone de message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p>Graisse de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur de ligne </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de texte dans le message. Affecte l’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Rembourrage intérieur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce message prend en charge le sélecteur d’attributs `state` avec les valeurs possibles suivantes : `verifyerror`, `senderror`et `sendsuccess`. La valeur `verifyerror` est définie lorsqu’un message est affiché en raison d’un échec de validation d’entrée en ligne. La valeur `senderror` est définie lorsqu’un service de messagerie principal signale une erreur. La `sendsuccess` valeur est définie lorsque le courrier électronique est envoyé avec succès. De cette façon, il est possible d’appliquer un style différent au message en fonction de l’état de la boîte de dialogue.

Le message d’erreur peut être localisé. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple - Pour configurer un message afin d’utiliser une police en gras de dix points, ayez une hauteur de ligne de 25 pixels et un remplissage de 20 pixels sur la gauche. Utilisez également une icône représentant un point d’exclamation, du texte rouge en cas d’erreur, ainsi qu’aucune icône et du texte vert en cas de réussite :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

Si un défilement vertical est nécessaire, la barre de défilement est rendue dans le panneau situé près du bord droit de la boîte de dialogue, qui est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogscrollpanel
```

**Propriétés CSS du panneau de défilement de la boîte de dialogue**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du panneau de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un panneau de défilement de 44 pixels de large :

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

L’aspect de la zone de la barre de défilement est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar
```

**Propriétés CSS de la barre de défilement**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de la barre de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p> La barre de défilement verticale est décalée par rapport au haut du panneau de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p> La barre de défilement verticale est décalée par rapport au bas du panneau de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Droite </span> </p> </td> 
   <td colname="col2"> <p> La barre de défilement horizontale est décalée par rapport au bord droit du panneau de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une barre de défilement de 28 pixels de large, avec une marge de huit pixels à partir du haut, de la droite et du bas du panneau de défilement :

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

La piste de la barre de défilement correspond à la zone située entre les boutons de défilement supérieur et inférieur. Le composant définit automatiquement la position et la hauteur de la piste. La piste est contrôlée par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**Propriétés CSS de la piste de défilement**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de voie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la piste. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer une piste de barre de défilement de 28 pixels de large avec un arrière-plan gris :

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Le pouce de la barre de défilement se déplace verticalement dans une zone de piste de défilement. Sa position verticale est entièrement contrôlée par la logique du composant, mais la hauteur du pouce ne change pas dynamiquement en fonction de la quantité de contenu. Vous pouvez configurer la hauteur du pouce et d’autres aspects à l’aide du sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**Propriétés CSS du pouce de la barre de défilement**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Dessus de rembourrage </span> </p> </td> 
   <td colname="col2"> <p> Le rembourrage vertical entre le haut de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Fond de rembourrage </span> </p> </td> 
   <td colname="col2"> <p> Remplissage vertical entre le bas de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état numérique donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniature prend en charge le sélecteur d’attributs`state`, qui peut être utilisé pour appliquer différents habillages à différents états du pouce : `up`, , `down``over`et `disabled`.

Les info-bulles des boutons peuvent être localisées. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple : pour configurer une barre de défilement de 28 x 45 pixels, avec une marge de dix pixels en haut et en bas et une illustration différente pour chaque état :

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

L’apparence des boutons de défilement supérieur et inférieur est contrôlée par les sélecteurs de classe CSS suivants :

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton  
  
```

**Propriétés CSS des boutons de défilement supérieur et inférieur**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
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
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ces boutons prennent en charge le sélecteur d’attributs`state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton : `up`, , `down``over`et `disabled`.

Exemple : pour configurer des boutons de défilement de 28 x 32 pixels avec des illustrations différentes pour chaque état :

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
