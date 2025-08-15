---
description: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 9ec5ed03-1d8f-4e67-a9a3-bdf160b105c5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# FavoritesView.fmt{#favoritesview-fmt}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le format d’image utilisé par le composant pour charger des images à partir d’Image Server. Le format est n’importe quelle valeur prise en charge par le serveur d’images et le navigateur du client. </p> <p>Si le format d’image se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images en tant que contenu transparent. Pour toutes les autres valeurs de format d’image, le composant traite les images comme étant opaques. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
