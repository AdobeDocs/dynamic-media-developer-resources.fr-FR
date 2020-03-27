---
description: En mode de zoom intégré, le principal se compose de l’image statique, de l’image agrandie affichée dans le de fenêtre déroulante  sur l’image statique et du message de pointe affiché au-dessus de l’image statique.
seo-description: En mode de zoom intégré, le principal se compose de l’image statique, de l’image agrandie affichée dans le de fenêtre déroulante  sur l’image statique et du message de pointe affiché au-dessus de l’image statique.
seo-title: Affichage de zoom déroulant
solution: Experience Manager
title: Affichage de zoom déroulant
topic: Dynamic media
uuid: c4c94432-7b6f-40a8-ae5f-9423234f3656
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Affichage de zoom déroulant{#flyout-zoom-view}

En mode de zoom intégré, le principal se compose de l’image statique, de l’image agrandie affichée dans le de fenêtre déroulante  sur l’image statique et du message de pointe affiché au-dessus de l’image statique.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect du principal est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7flyoutzoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du  principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour rendre le principal transparent :

```
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

L’aspect du message de conseil est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

Il est possible de configurer le style de police, l’aspect de la taille et le décalage vertical au moyen de CSS. Toutefois, l’alignement horizontal est géré par la logique du lecteur de contenu. Il n’est pas possible de le remplacer via CSS à l’aide de `left` ou de `right` propriétés.

**Propriétés CSS du message de conseil**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de fond d’arrière-plan du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Rayon de la bordure d’arrière-plan du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p> Décalage à partir du bas du  principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte du conseil. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p> Opacité de l’arrière-plan du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Remplissage autour du texte du message. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message d’info-bulle peut être localisé. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) de l’interface utilisateur.

Exemple - Pour configurer un message d’info-bulle semi-transparent avec une police Arial blanche de 12 px, décalage de 50 pixels par rapport au bas du principal, du remplissage et d’une bordure arrondie :

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```

