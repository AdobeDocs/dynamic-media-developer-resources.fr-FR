---
title: FavoritesView.favoritesThumbView
description: FavoritesView.favoritesThumbView
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 5c57fcc8-be67-408a-9c4c-4e15d5fe6410
TQID: 'https://experienceleague.adobe.com/o1SjDLDUYHn7ygVPxi5Af7ElhXgISpmoFANSuMf0xNk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 4%

---

# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`zone`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> zone </span></span> </p> </td> 
   <td colname="col2"> <p> Indique la zone de recadrage de la miniature des Favoris. Exprimé en valeur relative par rapport à la taille totale de l’image, avec une plage comprise entre <span class="codeph"> 0</span> et <span class="codeph"> 1,0</span>. </p> <p>Une valeur égale à <span class="codeph"> 1</span> signifie que l’image d’image entière est utilisée pour la miniature. </p> <p>Une valeur de <span class="codeph"> 0,1</span> signifie que seulement 10 % de la taille de l’image sont utilisés. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`0.1`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`favoritesThumbArea=0.5`
