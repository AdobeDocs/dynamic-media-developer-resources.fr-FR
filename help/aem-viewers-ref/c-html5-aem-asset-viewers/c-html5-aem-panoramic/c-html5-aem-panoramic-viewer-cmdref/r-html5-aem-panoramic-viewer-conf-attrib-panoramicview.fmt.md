---
title: PanoramicView.fmt
description: Indique le format d’image utilisé par le composant pour charger les images à partir du serveur d’images.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

Indique le format d’image utilisé par le composant pour charger les images à partir du serveur d’images. Si le format spécifié se termine par &quot;-alpha&quot;, le composant rend les images comme transparentes. Pour tous les autres formats d’image, le composant traite les images comme opaques. Notez que le composant dispose par défaut d’un arrière-plan transparent. Par conséquent, pour le rendre opaque, définissez la variable `background-color` Propriété CSS à `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> Spécifie le format d’image à utiliser par le composant pour le chargement des images à partir du serveur d’images. Si le format spécifié se termine par "-alpha", le composant effectue le rendu des images en tant que contenu transparent ; pour tous les autres formats d’image, le composant traite les images comme opaques. Notez que le composant dispose par défaut d’un arrière-plan transparent. Par conséquent, pour opaque, définissez la propriété CSS de couleur d’arrière-plan sur la couleur souhaitée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
