---
title: Info-bulles
description: Sur les ordinateurs de bureau, certains éléments de l’interface utilisateur tels que les boutons ont des info-bulles qui s’affichent au survol de la souris.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 25d4aa58-e16e-4b96-bca0-e98d542b7b81
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Info-bulles{#tooltips}

Sur les ordinateurs de bureau, certains éléments de l’interface utilisateur tels que les boutons ont des info-bulles qui s’affichent au survol de la souris.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone principale de la visionneuse**

L’apparence des info-bulles est contrôlée par le sélecteur de classe CSS suivant :

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> rayon de bordure </span> </p> </td> 
   <td colname="col2"> <p> Rayon de bordure d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur de bordure </span> </p> </td> 
   <td colname="col2"> <p> Couleur de la bordure d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de la police du texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Dans le cas où les styles d’info-bulle sont personnalisés à partir de la page Web d’incorporation, toutes les propriétés doivent contenir `!IMPORTANT` une règle. Cela n’est pas nécessaire si les info-bulles sont personnalisées dans le fichier CSS de la visionneuse.

Exemple : pour configurer des info-bulles dotées d’une bordure grise avec un rayon d’angle de 3 pixels, un arrière-plan noir et du texte blanc dans Arial, taille de 11 pixels :

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
