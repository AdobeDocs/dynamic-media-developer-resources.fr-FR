---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom intégré
role: Developer,User
exl-id: 6a9a5530-dbde-4090-8545-36bbd7322927
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le format d’image à utiliser par le composant pour le chargement des images à partir du serveur d’images. Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images en tant que contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. </p> <p>Notez que le composant a par défaut un arrière-plan blanc. Par conséquent, pour le rendre complètement transparent, définissez la propriété CSS <span class="codeph"> background-color</span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
