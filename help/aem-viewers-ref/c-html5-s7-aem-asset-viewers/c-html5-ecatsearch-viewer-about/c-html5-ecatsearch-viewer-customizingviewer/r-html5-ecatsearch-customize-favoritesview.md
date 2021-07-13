---
description: La vue Favoris est composée d’une colonne d’images miniatures.
solution: Experience Manager
title: Vue Favoris
feature: Dynamic Media Classic,Visionneuses,SDK/API,Recherche catalogue électronique
role: Developer,User
exl-id: 8daf3d19-615b-4d62-a6f5-6a153d193b88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---

# Vue Favoris{#favorites-view}

La vue Favoris est composée d’une colonne d’images miniatures.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

L’aspect du conteneur de vues favoris est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesview
```

La position et la hauteur de la vue Favoris sont gérées par la vue ; dans CSS, il est uniquement possible de définir la largeur.

**Propriétés CSS de la vue Favoris**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan de la vue Favoris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la vue. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une vue Favoris d’une largeur de 100 pixels avec un arrière-plan gris semi-transparent.

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

L’espacement entre les miniatures Favoris est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**Propriétés CSS des miniatures Favoris**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Taille de la marge verticale autour de chaque miniature. L’espacement réel des miniatures est égal à la somme de la marge supérieure et de la marge inférieure définie pour <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer l’espacement de 10 pixels.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

L’aspect des miniatures individuelles est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**Propriétés CSS des miniatures Favoris**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure de la miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniature prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de miniature. En particulier, `state="selected"` correspond à la miniature récemment sélectionnée par l’utilisateur. `state="default"` correspond au reste des miniatures. Et `state="over"` est utilisé lorsque vous pointez sur la souris.

Exemple : pour configurer des miniatures de 75 x 75 pixels, vous devez définir une bordure par défaut en gris clair et une bordure sélectionnée en gris foncé.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

L’aspect du libellé de la miniature est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**Propriétés CSS de l’étiquette Favoris**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer des libellés avec une police Helvetica de 14 pixels.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
