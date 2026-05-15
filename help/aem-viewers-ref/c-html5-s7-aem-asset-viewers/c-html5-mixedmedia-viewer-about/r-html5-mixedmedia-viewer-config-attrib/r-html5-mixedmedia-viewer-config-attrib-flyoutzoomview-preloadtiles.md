---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 041df5c7-9391-4dde-8988-a83272c7c438
TQID: 'https://experienceleague.adobe.com/VekzJdb-QLea1D4Db9lsA5jRmjCf-VUuwUoxeqUejEw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 7%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Définissez sur <span class="codeph"> 1</span> pour activer le préchargement de l’image agrandie. </p> <p>Définissez cette valeur sur <span class="codeph"> 0</span> pour charger l’image de zoom de manière incrémentielle, si nécessaire. </p> <p> <p>Si vous activez cette option, l’utilisation de la bande passante peut être considérablement plus élevée, car l’image agrandie doit être chargée dans son intégralité, même si l’utilisateur n’effectue aucune action de zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
