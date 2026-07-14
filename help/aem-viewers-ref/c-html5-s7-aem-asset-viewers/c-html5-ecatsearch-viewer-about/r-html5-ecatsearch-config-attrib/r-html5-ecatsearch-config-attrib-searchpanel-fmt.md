---
description: SearchPanel.fmt
solution: Experience Manager
title: SearchPanel.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a713b8f1-e834-457d-b038-eb30b25f905f
TQID: 'https://experienceleague.adobe.com/OW-iPLYzqFNCYHrlUBZ25wBQX1ZjNd1ddE-d1y29-d4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 67
ht-degree: 4%

---

# SearchPanel.fmt{#searchpanel-fmt}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Indique le format d’image utilisé par le composant pour charger des images à partir du serveur d’images. Il peut s’agir de n’importe quel format pris en charge par le serveur d’images et le navigateur client. </p> <p>Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images en tant que contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Facultatif.

## Par défaut {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## Exemple {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]

