---
title: Imprimer
description: L’outil Impression se compose d’un bouton ajouté à la barre de contrôle et de la boîte de dialogue modale qui s’affiche lorsque l’outil est activé.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 25057e72-f079-4221-91c2-760d99d30633
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '1488'
ht-degree: 0%

---

# Imprimer{#print}

L’outil Impression se compose d’un bouton ajouté à la barre de contrôle et de la boîte de dialogue modale qui s’affiche lorsque l’outil est activé.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect du bouton d’impression est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7print
```

**Propriétés CSS du bouton d’impression**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de la marge supérieure </span> </p> </td> 
   <td colname="col2"> <p> Décalage par rapport au haut de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la marge de gauche </span> </p> </td> 
   <td colname="col2"> <p> Distance par rapport au bouton suivant à gauche, ou sur le côté gauche de la barre de contrôle s’il s’agit du premier bouton d’une ligne. </p> </td> 
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
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - Pour configurer un bouton d’impression de 28 x 28 pixels qui affiche une image différente pour chacun des quatre états de bouton.

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

Le recouvrement d’arrière-plan qui couvre la page web lorsque la boîte de dialogue est active est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**Propriétés CSS du recouvrement principal**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p> Opacité de la superposition d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur de recouvrement de l’arrière-plan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer la superposition de l’arrière-plan en gris avec une opacité de 70 % :

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Par défaut, la boîte de dialogue modale s’affiche centrée sur l’écran sur les ordinateurs de bureau. Le positionnement et le dimensionnement de la boîte de dialogue sont gérés par le composant . La boîte de dialogue est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**Propriétés CSS de la boîte de dialogue**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rayon de bordure </span> </p> </td> 
   <td colname="col2"> <p> Rayon de bordure de la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan de la boîte de dialogue ; </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer une boîte de dialogue de sorte qu’elle ait un arrière-plan gris :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

L’en-tête de boîte de dialogue se compose d’une icône, d’un texte de titre et d’un bouton Fermer. Le conteneur d’en-tête est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
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

L’icône et le texte du titre sont placés dans un conteneur supplémentaire contrôlé par ce qui suit :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**Propriétés CSS de la ligne de boîte de dialogue**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure de l’icône d’en-tête et du titre. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icône d’en-tête est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
```

**Propriétés CSS de l’icône d’en-tête de boîte de dialogue**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
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
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le titre de l’en-tête est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
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
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton Fermer et le titre de la boîte de dialogue peuvent être localisés. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - Pour configurer l’en-tête de boîte de dialogue avec un remplissage, une icône de 22 x 22 pixels et un titre en gras de 16 points. Enfin, un bouton Fermer de 28 x 28 pixels positionné à deux pixels du haut et à deux pixels de la droite du conteneur de boîte de dialogue :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Le pied de boîte de dialogue se compose des boutons Annuler et Envoyer pour impression. Le conteneur de pied de page est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
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

Le pied de page comporte un conteneur intérieur qui permet de conserver les deux boutons. Elle est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
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

Le bouton Envoyer à imprimer est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**Propriétés CSS du bouton d’action de boîte de dialogue**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
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

Les info-bulles des boutons peuvent être localisées. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - pour configurer un pied de boîte de dialogue avec un bouton Annuler de 64 x 34 et un bouton Envoyer à l’impression de 96 x 34, avec la couleur du texte et la couleur d’arrière-plan différentes pour chaque état de bouton :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

La zone de dialogue principale, entre l’en-tête et le pied de page, contient le contenu de la boîte de dialogue. Dans tous les cas, le composant gère la largeur de cette zone. Il n’est pas possible de la définir dans CSS. La zone de dialogue principale est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**Propriétés CSS de la zone d’affichage de la boîte de dialogue**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de la zone de la boîte de dialogue principale. </p> </td> 
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

Exemple : pour configurer une zone de boîte de dialogue principale afin d’avoir une hauteur calculée automatiquement, ayez une marge de dix pixels et utilisez un arrière-plan blanc :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

Tout le contenu du formulaire (comme les libellés et les champs de saisie) réside dans un conteneur contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

**Propriétés CSS du corps de la boîte de dialogue &#x200B;**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Rembourrage intérieur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer le contenu d’un formulaire avec un remplissage de dix pixels :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

Le formulaire de boîte de dialogue est rempli ligne par ligne, chaque ligne portant une partie du contenu du formulaire (comme une étiquette et un champ de saisie de texte). La ligne de formulaire unique est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

La taille du bloc de contenu de boîte de dialogue est contrôlée par le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**Propriétés CSS de la boîte de dialogue input width**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bloc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir un bloc de contenu sur une largeur de 430 pixels et une marge intérieure de 10 pixels en bas :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Tous les libellés statiques du formulaire de boîte de dialogue sont contrôlés avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

Cette classe ne convient pas pour contrôler la taille ou la position des libellés, car vous pouvez l’appliquer à des textes à différents endroits dans l’interface utilisateur du formulaire.

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

Les libellés des boîtes de dialogue peuvent être localisés. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - pour configurer toutes les étiquettes en gris, gras, avec une police de neuf pixels :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Les commandes de saisie sont encapsulées dans le conteneur et contrôlées avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**Propriétés CSS du conteneur d’entrée de boîte de dialogue**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure gauche </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir une marge intérieure de 30 pixels à partir du bord gauche de la boîte de dialogue.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

Les boutons radio et leur texte de légende sont contrôlés avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**Propriétés CSS de l’option de boîte de dialogue**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur totale du bouton radio avec une légende. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte de la légende. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’espacement entre le bouton radio et sa légende est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**Propriétés CSS de la boîte de dialogue, option entrée**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> de la marge droite </p> </td> 
   <td colname="col2"> <p> Espace entre le bouton radio et sa légende. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les sélecteurs numériques pour la sélection de la plage d’impression sont contrôlés avec le sélecteur de classe CSS suivant

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**Propriétés CSS de la plage d’impression de la boîte de dialogue**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du sélecteur numérique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de la marge </span> </p> </td> 
   <td colname="col2"> <p> Espacement autour du sélecteur numérique. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer tous les boutons radio sur une largeur de 150 pixels avec du texte noir, un espacement de dix pixels et des sélecteurs numériques de 42 pixels de large :

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

Le séparateur horizontal entre la sélection de la plage de pages et la disposition d’impression est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**Propriétés CSS du séparateur horizontal**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de bordure </span> </p> </td> 
   <td colname="col2"> <p> Bordure autour du séparateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du séparateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de la marge </span> </p> </td> 
   <td colname="col2"> <p>Marge externe </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer un diviseur gris de 430 pixels de largeur avec un remplissage vertical de 10 pixels des deux côtés et une marge de dix pixels en haut :

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```
