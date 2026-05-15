---
title: Vue Favoris
description: La vue Favoris se compose d’une colonne d’images miniatures.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
TQID: 'https://experienceleague.adobe.com/jOrrq3rLoXwGWAKAcafCkv2twn-N-PE5jbEqQpZI9WQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 295
ht-degree: 0%

---

# Vue Favoris{#favorites-view}

La vue Favoris se compose d’une colonne d’images miniatures.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

L’aspect du conteneur d’affichage Favoris est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesview
```

La position et la hauteur de la vue Favoris sont gérées par la vue ; dans CSS, il n’est possible de définir que la largeur.

**Propriétés CSS de la vue Favoris**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan de la vue Favoris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la vue. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer une vue des Favoris d’une largeur de 100 pixels avec un arrière-plan gris semi-transparent :

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

L’espacement entre les miniatures des Favoris est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**Propriétés CSS des miniatures de favoris**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Taille de la marge verticale autour de chaque miniature. L’espacement réel des miniatures est égal à la somme des marges supérieure et inférieure définies pour <span class="codeph">’</span> .s7thumbcell. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer l’espacement de dix pixels :

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

L’aspect de chaque miniature est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**Propriétés CSS des miniatures de favoris**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Bordure de la miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniature prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de miniature. En particulier, `state="selected"` correspond à la miniature récemment sélectionnée par l&#39;utilisateur. L’attribut `state="default"` correspond au reste des miniatures. De plus, l’attribut `state="over"` est utilisé lors du survol de la souris.

Exemple - Pour configurer des miniatures de 75 x 75 pixels, elles doivent avoir une bordure par défaut gris clair et une bordure sélectionnée gris foncé :

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

L’aspect du libellé de la miniature est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**Propriétés CSS du libellé Favoris**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer des libellés avec une police Helvetica® de 14 pixels :

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
