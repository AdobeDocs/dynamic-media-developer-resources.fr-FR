---
title: Swatches.fmt
description: Swatches.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 043196c8-63ab-439e-a28f-b76d1467f26e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Spécifie le format d’image utilisé par le composant pour charger les images à partir d’Image Server. Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images en tant que contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. Le composant possède un arrière-plan blanc par défaut. Par conséquent, pour rendre l’arrière-plan transparent, définissez la propriété CSS de couleur d’arrière-plan <span class="codeph"></span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt-png-alpha`
