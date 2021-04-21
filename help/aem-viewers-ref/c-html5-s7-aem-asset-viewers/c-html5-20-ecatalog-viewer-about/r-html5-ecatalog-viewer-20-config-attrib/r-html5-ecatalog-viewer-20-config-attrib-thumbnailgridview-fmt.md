---
description: ThumbnailGridView.fmt
solution: Experience Manager
title: ThumbnailGridView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

`[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Indique le format d’image utilisé par le composant pour le chargement des images à partir du serveur Image Server. Il peut s’agir de toute valeur prise en charge par Image Server et le navigateur client. Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images sous forme de contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

Facultatif.

## Par défaut {#section-502c098dbae1452180c7f575a1d9dc8b}

`jpeg`

## Exemple {#section-5cde7b856ba646c293cfd3d79e47c507}

`fmt-png-alpha`
