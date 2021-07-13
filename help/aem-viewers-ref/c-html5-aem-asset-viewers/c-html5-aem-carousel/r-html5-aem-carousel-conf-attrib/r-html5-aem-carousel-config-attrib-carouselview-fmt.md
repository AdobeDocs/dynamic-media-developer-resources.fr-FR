---
description: CarouselView.fmt
solution: Experience Manager
title: CarouselView.fmt
feature: Dynamic Media Classic,Visionneuses,SDK/API,Bannières de carrousel
role: Developer,User
exl-id: a43ca095-2a59-4a0c-a460-f465cbd4ed5f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 5%

---

# CarouselView.fmt{#carouselview-fmt}

`[CarouselView.|<containerId>_carouselView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Indique le format d’image que le composant utilise pour charger les images à partir du serveur d’images. </p> <p>Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images en tant que contenu transparent. </p> <p>Pour tous les autres formats d’image, le composant traite les images comme opaques. Par défaut, l’arrière-plan du composant est blanc. Par conséquent, pour le rendre transparent, définissez la propriété CSS <span class="codeph"> background-color</span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
