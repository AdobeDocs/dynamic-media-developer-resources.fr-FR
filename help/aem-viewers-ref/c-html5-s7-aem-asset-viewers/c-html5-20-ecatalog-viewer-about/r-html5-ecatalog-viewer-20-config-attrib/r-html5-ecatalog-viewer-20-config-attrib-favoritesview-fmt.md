---
title: FavoritesView.fmt
description: FavoritesView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d14f8a0c-5fb5-4315-ba8b-79add6d389b0
TQID: 'https://experienceleague.adobe.com/6S08OFzBR3Hep6DWq2O681ynxX-mmdx71Svu07TjftU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 72
ht-degree: 4%

---

# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Indique le format d’image utilisé par le composant pour charger les images à partir du serveur d’images. Le format correspond à toute valeur prise en charge par le serveur d’images et le navigateur client. </p> <p>Si le format d’image se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images en tant que contenu transparent. Pour toutes les autres valeurs de format d’image, le composant traite les images comme opaques. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
