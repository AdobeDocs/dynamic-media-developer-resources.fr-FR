---
title: Partage twitter
description: L’outil de partage twitter se compose d’un bouton ajouté au panneau Partage sur les réseaux sociaux. Lorsque le bouton est sélectionné, l’utilisateur est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil Partage sur les réseaux sociaux .
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Partage twitter{#twitter-share}

L’outil de partage twitter se compose d’un bouton ajouté au panneau Partage sur les réseaux sociaux. Lorsque le bouton est sélectionné, l’utilisateur est redirigé vers une boîte de dialogue de partage fournie par un service social. La position du bouton est entièrement gérée par l’outil Partage sur les réseaux sociaux .

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L’aspect du bouton Partage Twitter est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7twittershare
```

**Propriétés CSS de l’outil de partage Twitter**

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
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge `state` sélecteur d’attributs qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Il est possible de supprimer le bouton du panneau Partage sur les réseaux sociaux en définissant `display:none` Propriété CSS sur sa classe CSS.

L’info-bulle de bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) pour plus d’informations.

Exemple : pour configurer un bouton de partage Twitter de 28 x 28 pixels et afficher une image différente pour chacun des quatre états de bouton différents :

```
.s7smartcropvideoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
