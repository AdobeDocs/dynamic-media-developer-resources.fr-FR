---
title: ZoomView.fmt
description: Indique le format d’image que le composant utilise pour charger les images à partir du serveur d’images.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 6a023abb-71c7-4db5-8d05-bf0a4b1fc3a0
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---

# ZoomView.fmt{#zoomview-fmt}

Indique le format d’image que le composant utilise pour charger les images à partir du serveur d’images.

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images en tant que contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. Par défaut, l’arrière-plan du composant est blanc. Par conséquent, pour le rendre transparent, définissez la propriété CSS <span class="codeph"> background-color</span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
