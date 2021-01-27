---
description: L’outil de partage de courrier électronique est constitué d’un bouton ajouté au panneau de partage Social et de la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil de partage Social.
seo-description: L’outil de partage de courrier électronique est constitué d’un bouton ajouté au panneau de partage Social et de la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil de partage Social.
seo-title: Partage de courrier électronique
solution: Experience Manager
title: Partage de courrier électronique
topic: Dynamic Media
uuid: fc60dd7b-651e-458c-9057-693ca1c0afdc
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '3073'
ht-degree: 1%

---


# Partage de courrier électronique{#email-share}

L’outil de partage de courrier électronique est constitué d’un bouton ajouté au panneau de partage Social et de la boîte de dialogue modale qui s’affiche lorsque l’outil est activé. La position du bouton est entièrement gérée par l’outil de partage Social.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect du bouton de partage de courrier électronique est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emailshare
```

**Propriétés CSS de l’outil de partage de courrier électronique**

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
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau de partage Social en définissant la propriété `display:none` CSS sur sa classe CSS.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un bouton de partage de courrier électronique de 28 x 28 pixels et qui affiche une image différente pour chacun des quatre états de bouton différents.

```
.s7ecatalogsearchviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

L’incrustation d’arrière-plan qui couvre la page Web lorsque la boîte de dialogue est principale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay
```

**Propriétés CSS de l’incrustation arrière**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité  </span> </p> </td> 
   <td colname="col2"> <p> Opacité de l’incrustation en arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’incrustation d’arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer l’incrustation d’arrière-plan en gris avec une opacité de 70 % :

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Par défaut, la boîte de dialogue modale s’affiche centrée sur l’écran des systèmes de bureau et occupe l’ensemble de la zone de page Web sur les périphériques tactiles. Dans tous les cas, le positionnement et le dimensionnement de la boîte de dialogue sont gérés par le composant. La boîte de dialogue est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialog
```

**Propriétés CSS de la boîte de dialogue**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> rayon de la bordure de la boîte de dialogue (au cas où la boîte de dialogue ne prendrait pas la totalité de la fenêtre du navigateur); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d'arrière-plan de la boîte de dialogue ; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Doit être soit désactivée, soit définie à 100 %, auquel cas la boîte de dialogue prend la totalité de la fenêtre du navigateur (ce mode est préféré sur les périphériques tactiles); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p> Doit être soit désactivée, soit définie à 100 %, auquel cas la boîte de dialogue prend la totalité de la fenêtre du navigateur (ce mode est préféré sur les périphériques tactiles). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une boîte de dialogue permettant d’utiliser toute la fenêtre du navigateur et d’avoir un arrière-plan blanc sur les périphériques tactiles :

```
.s7ecatalogsearchviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L&#39;en-tête de la boîte de dialogue se compose d&#39;une icône, d&#39;un texte de titre et d&#39;un bouton de fermeture. Le conteneur d’en-tête est contrôlé à l’aide du sélecteur de classe CSS suivant.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**Propriétés CSS de la ligne de dialogue**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure de l’icône et du titre de l’en-tête. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icône d’en-tête est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon
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
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le titre d’en-tête est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton
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
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton Fermer et le titre de la boîte de dialogue peuvent être localisés. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un en-tête de boîte de dialogue avec remplissage, une icône de 24 x 17 pixels, un titre en gras de 16 points et un bouton Fermer de 28 x 28 pixels positionné à deux pixels du haut et à deux pixels de la droite du conteneur de boîte de dialogue :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Le pied de page de la boîte de dialogue se compose des boutons Annuler et Envoyer un courrier électronique. Le conteneur de pied de page est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter
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

Le pied de page comporte un conteneur interne qui conserve les deux boutons. Il est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer
```

**Propriétés CSS du conteneur de bouton de la boîte de dialogue**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre le pied de page et les boutons. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton Annuler est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton
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
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Le bouton Envoyer un courrier électronique est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton
```

**Propriétés CSS du bouton d’action de la boîte de dialogue**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button
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

Les info-bulles de ces boutons peuvent être localisées. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un pied de page de boîte de dialogue avec un bouton Annuler de 64 x 34 et un bouton Envoyer un courriel de 82 x 34, la couleur du texte et la couleur d’arrière-plan étant différentes pour chaque état de bouton :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

La zone de dialogue principale (entre l’en-tête et le pied de page) contient le contenu de la boîte de dialogue défilante et le panneau de défilement sur la droite. Dans tous les cas, le composant gère la largeur de cette zone, il n&#39;est pas possible de la définir dans CSS. La zone de dialogue principale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea
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

>[!NOTE]
>
>La zone de boîte de dialogue principale prend en charge le sélecteur d’attributs `state` facultatif. Il est défini sur `sendsuccess` lorsque le formulaire de courrier électronique est envoyé et que la boîte de dialogue affiche un message de confirmation. Tant que le message de confirmation est petit, ce sélecteur d’attributs peut être utilisé pour réduire la hauteur de la boîte de dialogue lorsque ce message de confirmation s’affiche.

Exemple : pour configurer la zone de la boîte de dialogue principale de manière à ce qu’elle soit de 300 pixels de hauteur au départ et de 100 pixels de hauteur lorsque le message de confirmation s’affiche, ayez une marge de dix pixels et utilisez un arrière-plan blanc :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

Tout le contenu du formulaire (comme les libellés et les champs de saisie) se trouve dans un conteneur contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody
```

Si la hauteur de ce conteneur semble supérieure à la zone de boîte de dialogue principale, un défilement vertical est activé automatiquement par le composant.

**Propriétés CSS du corps de la boîte de dialogue **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer le contenu du formulaire de sorte qu’il ait un remplissage de dix pixels :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

Le formulaire de boîte de dialogue est rempli ligne par ligne, où chaque ligne porte une partie du contenu du formulaire (comme un libellé et un champ de saisie de texte). Une seule ligne de formulaire est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**Propriétés CSS de la ligne de boîte de dialogue**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer un formulaire de boîte de dialogue avec un remplissage de dix pixels pour chaque ligne :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Tous les libellés statiques du formulaire de boîte de dialogue sont contrôlés avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel
```

Cette classe n’est pas adaptée au contrôle de la taille ou de la position des libellés, car vous pouvez l’appliquer à des textes situés à divers endroits de l’interface utilisateur du formulaire.

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

Les étiquettes de boîte de dialogue peuvent être localisées. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour définir toutes les étiquettes en gris, en gras, avec une police de neuf pixels :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Tous les libellés statiques affichés à gauche des champs d’entrée de formulaire sont contrôlés avec :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel
```

**Propriétés CSS du libellé d’entrée de la boîte de dialogue**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du libellé statique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement de texte  </span> </p> </td> 
   <td colname="col2"> <p>Alignement horizontal du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p>Marge statique du libellé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure statique du libellé. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir des libellés de champ d’entrée d’une largeur de 50 pixels, alignés à droite, avec dix pixels de remplissage et une marge de dix pixels à droite :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Chaque champ de saisie de formulaire est encapsulé dans le conteneur, ce qui vous permet d’appliquer une bordure personnalisée autour du champ de saisie. Il est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer
```

**Propriétés CSS du conteneur d’entrée de la boîte de dialogue**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure autour du conteneur du champ d’entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le conteneur de champ d’entrée prend en charge le sélecteur d’attributs `state` facultatif. Il est défini sur `verifyerror` lorsque l’utilisateur commet une erreur dans le format de données d’entrée et que la validation en ligne échoue. Ce sélecteur d’attributs peut être utilisé pour mettre en surbrillance les entrées utilisateur incorrectes dans le formulaire.

La plupart des champs d’entrée qui s’étendent de l’étiquette à gauche jusqu’au bord droit du corps de la boîte de dialogue (y compris le champ De et le champ Message) sont contrôlés à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide
```

**Propriétés CSS du champ large d’entrée de la boîte de dialogue**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du champ d’entrée. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le champ À est plus étroit car il alloue de l’espace au bouton Supprimer l’e-mail sur la droite. Il est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort
```

**Propriétés CSS du champ court de saisie de la boîte de dialogue**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du champ d’entrée. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un formulaire avec une bordure grise d’un pixel et un remplissage de neuf pixels autour de tous les champs de saisie ; pour avoir la même bordure en rouge pour les champs dont la validation a échoué, pour avoir un champ de saisie de 250 pixels de large et le reste des champs de saisie de 300 pixels de large :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

Le champ de saisie de message électronique est en outre contrôlé par :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage
```

Cette classe vous permet de définir des propriétés spécifiques pour l&#39;élément `TEXTAREA` sous-jacent.

**Propriétés CSS du message de la boîte de dialogue**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> retour à la ligne  </span> </p> </td> 
   <td colname="col2"> <p>Style d’encapsulation des mots. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer un message électronique d’une hauteur de 50 pixels et utiliser le retour à la ligne `break-word` :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

Le bouton Ajouter une autre adresse électronique permet à un utilisateur d’ajouter plusieurs destinataires dans un formulaire électronique. Il est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton
```

**Propriétés CSS de la boîte de dialogue Ajouter un bouton d’adresse électronique**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte des boutons pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Image de bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p>Position de l’image du bouton dans la zone du bouton. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>Hauteur du texte à l’intérieur du bouton. Affecte l’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement de texte  </span> </p> </td> 
   <td colname="col2"> <p>Alignement horizontal du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer le bouton &quot;Ajouter une autre adresse électronique&quot; à une hauteur de 25 pixels, utilisez une police en gras de 12 points avec un alignement à droite et une couleur et une image de texte différentes pour chaque état :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

Le bouton Supprimer permet à un utilisateur de supprimer des destinataires supplémentaires du formulaire de courrier électronique. Il est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton
```

**Propriétés CSS de la boîte de dialogue supprimer le bouton de courrier électronique**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Image de bouton pour chaque état. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un bouton Supprimer à 25 x 25 pixels et utiliser une image différente pour chaque état :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

Le contenu partagé s’affiche dans la partie inférieure du corps de la boîte de dialogue et comprend une miniature, un titre, une URL d’origine et une description. Il est encapsulé dans un conteneur contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**Propriétés CSS du contenu de la boîte de dialogue **

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure du conteneur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un conteneur inférieur de sorte qu’il ait une bordure en pointillé d’un pixel et aucun remplissage :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

L’image miniature est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail
```

La propriété `background-image` est définie par la logique du composant.

**Propriétés CSS de l’image miniature de la boîte de dialogue**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement vertical  </span> </p> </td> 
   <td colname="col2"> <p>Miniature d’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer la miniature à 90 x 60 pixels et l’aligner en haut avec dix pixels de remplissage :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

Le titre, l’origine et la description du contenu sont ensuite regroupés dans un panneau à droite de la miniature de contenu. Il est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel
```

**Propriétés CSS du panneau d’informations de la boîte de dialogue**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un panneau d’informations sur le contenu d’une largeur de 300 pixels :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

Le titre du contenu est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle
```

**Propriétés CSS du titre de la boîte de dialogue**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-poids  </span> </p> </td> 
   <td colname="col2"> <p>Poids des polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un titre de contenu afin d’utiliser une police en gras et d’avoir une marge de dix pixels :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

L’origine du contenu est contrôlée à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin
```

**Propriétés CSS de l’origine de contenu de la boîte de dialogue **

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-poids  </span> </p> </td> 
   <td colname="col2"> <p>Poids des polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer l’origine de contenu de sorte qu’elle ait une marge de dix pixels :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

La description du contenu est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription
```

**Propriétés CSS de la description du contenu de la boîte de dialogue**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p>Marge extérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-poids  </span> </p> </td> 
   <td colname="col2"> <p>Poids des polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir une description de contenu avec une marge de dix pixels et une police de neuf points :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

Lorsqu’un utilisateur saisit des données d’entrée incorrectes et que la validation en ligne échoue, ou que la boîte de dialogue doit afficher une erreur ou un message de confirmation lors de l’envoi du formulaire, un message s’affiche en haut du corps de la boîte de dialogue. Il est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage
```

**Propriétés CSS du message d’erreur de la boîte de dialogue**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Icône Erreur. La valeur par défaut est un point d’exclamation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Position de l’icône d’erreur dans la zone de message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-poids  </span> </p> </td> 
   <td colname="col2"> <p>Poids des polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ligne-hauteur  </span> </p> </td> 
   <td colname="col2"> <p> Hauteur du texte dans le message. Affecte l’alignement vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce message prend en charge le sélecteur d’attributs `state` avec les valeurs possibles suivantes : `verifyerror`, `senderror` et `sendsuccess`. `verifyerror` est défini lorsqu’un message s’affiche en raison d’un échec de validation d’entrée en ligne ;  `senderror` est définie lorsqu’un service de messagerie principal signale une erreur ;  `sendsuccess` est définie lorsque le courrier électronique est envoyé avec succès. Il est ainsi possible de mettre le message différemment en fonction de l’état de la boîte de dialogue.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un message afin qu’il utilise une police en caractères gras de dix points, une hauteur de ligne de 25 pixels, un remplissage de 20 pixels à gauche, une icône de point d’exclamation, un texte rouge en cas d’erreur et aucune icône et un texte vert en cas de réussite :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

Si un défilement vertical est nécessaire, la barre de défilement est générée dans le panneau situé près du bord droit de la boîte de dialogue, qui est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel
```

**Propriétés CSS du panneau de défilement de la boîte de dialogue**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du panneau de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un panneau de défilement d’une largeur de 44 pixels :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

L’aspect de la zone de barre de défilement est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar
```

**Propriétés CSS de la barre de défilement**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Largeur de la barre de défilement. </p> </td> 
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

Exemple : pour configurer une barre de défilement de 28 pixels de large, avec une marge de huit pixels en haut, à droite et en bas du panneau de défilement :

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Le suivi de la barre de défilement est la zone située entre les boutons de défilement supérieur et inférieur. Le composant définit automatiquement la position et la hauteur de la piste. Le suivi est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**Propriétés CSS de la piste de défilement**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du suivi. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une piste de barre de défilement de 28 pixels de large et dont l’arrière-plan est gris :

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Le curseur de la barre de défilement se déplace verticalement dans une zone de défilement. Sa position verticale est entièrement contrôlée par la logique du composant, mais la hauteur du pouce ne change pas dynamiquement en fonction de la quantité de contenu. Vous pouvez configurer la hauteur du pouce et d’autres aspects à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**Propriétés CSS du curseur de la barre de défilement**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>La hauteur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage-haut  </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure verticale entre le haut de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage-bas  </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure verticale entre le bas de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de pouce donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de pouce : `up`, `down`, `over` et `disabled`.

Exemple : pour configurer le curseur de la barre de défilement de 28 x 45 pixels, avec une marge de dix pixels en haut et en bas et une illustration différente pour chaque état :

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

L’aspect des boutons de défilement supérieur et inférieur est contrôlé par les sélecteurs de classe CSS suivants :

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

Il n’est pas possible de positionner les boutons de défilement à l’aide des propriétés CSS `top`, `left`, `bottom` et `right`. La logique du lecteur les positionne automatiquement.

**Propriétés CSS des boutons de défilement supérieur et inférieur**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
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
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ces boutons prennent en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton : `up`, `down`, `over` et `disabled`.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer des boutons de défilement de 28 x 32 pixels et présentant des illustrations différentes pour chaque état :

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

