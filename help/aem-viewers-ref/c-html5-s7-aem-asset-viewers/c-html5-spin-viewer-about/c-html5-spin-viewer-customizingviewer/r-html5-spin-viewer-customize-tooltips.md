---
title: Infobulles
description: Sur les systèmes de bureau, certains éléments de l’interface utilisateur tels que les boutons comportent des infobulles qui s’affichent lorsque vous pointez dessus.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 1bc1a67b-7345-44bc-aed9-d20a61929e21
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# Infobulles{#tooltips}

Sur les systèmes de bureau, certains éléments de l’interface utilisateur tels que les boutons comportent des infobulles qui s’affichent lorsque vous pointez dessus.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

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
   <td colname="col2"> <p> Rayon de la bordure de fond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> Couleur de bordure de l’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
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
>Si les styles d’info-bulle sont personnalisés dans la page web d’intégration, toutes les propriétés doivent contenir `!IMPORTANT` règle. Cette règle n’est pas nécessaire si des info-bulles sont personnalisées dans le fichier CSS de la visionneuse.

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
