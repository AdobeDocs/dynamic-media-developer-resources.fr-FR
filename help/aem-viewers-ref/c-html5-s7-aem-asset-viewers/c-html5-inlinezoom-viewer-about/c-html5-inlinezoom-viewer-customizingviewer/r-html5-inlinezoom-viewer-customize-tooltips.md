---
title: Tooltips
description: Sur les systèmes de bureau, certains éléments de l’interface utilisateur tels que les boutons comportent des infobulles qui s’affichent lorsque vous pointez dessus.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: bcbdd047-428b-48f8-9bd9-600f36f2e0b7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# Infobulles{#tooltips}

On desktop systems, some user interface elements like buttons have tooltips that are displayed on mouse hover.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties of the main viewer area**

L’aspect des info-bulles est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7tooltip
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Background border radius. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> Couleur de bordure de l’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Couleur de fond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police du texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>In case tooltip styles are customized from within the embedding web page, all properties have to contain `!IMPORTANT` rule. Toutefois, il n’est pas nécessaire que les info-bulles soient personnalisées dans le fichier CSS de la visionneuse.

Exemple : pour configurer des info-bulles avec une bordure grise avec un rayon d’angle de 3 pixels, un arrière-plan noir et un texte blanc écrits en Arial® d’une taille de 11 pixels :

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
