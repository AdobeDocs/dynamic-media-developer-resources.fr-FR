---
title: Infobulles
description: Sur les ordinateurs de bureau, certains éléments de l’interface utilisateur tels que les boutons comportent des info-bulles qui s’affichent lorsque vous pointez dessus.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 78cc0f11-bec2-495e-b3c9-a91b6bd1b1f0
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# Infobulles{#tooltips}

Sur les ordinateurs de bureau, certains éléments de l’interface utilisateur tels que les boutons comportent des info-bulles qui s’affichent lorsque vous pointez dessus.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect des infobulles est contrôlé avec le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> de rayon de bordure </span> </p> </td> 
   <td colname="col2"> <p> Rayon de la bordure d'arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur de bordure </span> </p> </td> 
   <td colname="col2"> <p> Couleur de la bordure d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur de fond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> famille de polices </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police du texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Si les styles d’info-bulle sont personnalisés à partir de la page web d’incorporation, toutes les propriétés doivent contenir une règle de `!IMPORTANT`. Cette règle n’est pas nécessaire si les infobulles sont personnalisées dans le fichier CSS de la visionneuse.

Exemple - pour configurer des info-bulles dont la bordure grise présente un rayon de coin de 3 px, un arrière-plan noir et un texte blanc écrit en Arial®, taille de 11 pixels :

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
