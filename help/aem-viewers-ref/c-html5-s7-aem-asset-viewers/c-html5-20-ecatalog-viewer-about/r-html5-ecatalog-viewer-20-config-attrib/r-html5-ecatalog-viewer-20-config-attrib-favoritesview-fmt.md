---
description: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
topic: Dynamic Media
uuid: 4d9d161e-e39b-4607-9fb1-9dbfb06d7704
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 5%

---


# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Indique le format d’image utilisé par le composant pour le chargement des images à partir du serveur Image Server. Le format correspond à toute valeur prise en charge par le serveur d’images et le navigateur client. </p> <p>Si le format d’image se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images sous forme de contenu transparent. Pour toutes les autres valeurs de format d’image, le composant traite les images comme opaques. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
