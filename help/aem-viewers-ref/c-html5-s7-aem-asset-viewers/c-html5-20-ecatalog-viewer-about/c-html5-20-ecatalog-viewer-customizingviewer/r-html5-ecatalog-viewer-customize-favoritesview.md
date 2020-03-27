---
description: Le  Favoris se compose d’une colonne d’images miniatures.
seo-description: Le  Favoris se compose d’une colonne d’images miniatures.
seo-title: ' Favoris'
solution: Experience Manager
title: ' Favoris'
topic: Dynamic media
uuid: 6b954bec-0678-4970-b83a-c2d8fea06a25
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


#  Favoris{#favorites-view}

Le  Favoris se compose d’une colonne d’images miniatures.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

L’aspect du Favoris  est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesview
```

La position et la hauteur du  Favoris sont gérées par le ; dans CSS, il est uniquement possible de définir la largeur.

**Propriétés CSS du Favoris**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du  Favoris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du  du. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un  Favoris de 100 pixels de large avec un arrière-plan gris semi-transparent.

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

L’espacement entre les miniatures Favoris est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**Propriétés CSS des miniatures Favoris**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Taille de la marge verticale autour de chaque miniature. L’espacement réel des miniatures est égal à la somme de la marge supérieure et inférieure définie pour <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour définir un espacement de 10 pixels.

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

L’aspect d’une miniature individuelle est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**Propriétés CSS des miniatures Favoris**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure de la vignette. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniature prend en charge le sélecteur d’ `state` attributs, qui peut être utilisé pour appliquer différents habillages à différents états de miniature. En particulier, `state="selected"` correspond à la miniature récemment sélectionnée par l’utilisateur. `state="default"` correspond au reste des miniatures. Et `state="over"` est utilisé lorsque vous passez la souris.

Exemple : pour configurer des miniatures de 75 x 75 pixels, utilisez une bordure par défaut gris clair et une bordure sélectionnée gris foncé.

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

L’aspect du libellé de miniature est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**Propriétés CSS du libellé Favoris**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer des libellés avec une police Helvetica de 14 pixels.

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

