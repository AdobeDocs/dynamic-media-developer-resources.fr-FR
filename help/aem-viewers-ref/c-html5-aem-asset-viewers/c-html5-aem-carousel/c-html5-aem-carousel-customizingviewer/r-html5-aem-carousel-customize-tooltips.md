---
description: Sur les systèmes de bureau, certains éléments de l’interface utilisateur, tels que les boutons, comportent des info-bulles qui s’affichent lorsque vous pointez la souris.
seo-description: Sur les systèmes de bureau, certains éléments de l’interface utilisateur, tels que les boutons, comportent des info-bulles qui s’affichent lorsque vous pointez la souris.
seo-title: Info-bulles
solution: Experience Manager
title: Info-bulles
topic: Dynamic Media
uuid: c720c896-e540-4c1e-a0dc-31cc0300fea8
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# Info-bulles{#tooltips}

Sur les systèmes de bureau, certains éléments de l’interface utilisateur, tels que les boutons, comportent des info-bulles qui s’affichent lorsque vous pointez la souris.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visualisation principale**

L’aspect des info-bulles est contrôlé à l’aide du sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Rayon de la bordure d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p> Couleur de bordure d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur de fond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police du texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Si les styles d’info-bulle sont personnalisés à partir de la page Web incorporée, toutes les propriétés doivent contenir la règle `!IMPORTANT`. Cela n’est pas nécessaire si les info-bulles sont personnalisées dans le fichier CSS du lecteur de contenu.

Exemple : pour configurer des info-bulles avec une bordure grise d’un rayon d’angle de 3 pixels, un arrière-plan noir et un texte blanc en Arial de 11 pixels :

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

