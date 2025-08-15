---
title: PanoramicView.fmt
description: Spécifie le format d’image utilisé par le composant pour charger des images à partir d’Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

Spécifie le format d’image utilisé par le composant pour charger des images à partir d’Image Server. Si le format spécifié se termine par « -alpha », le composant effectue le rendu des images transparentes. Pour tous les autres formats d’image, le composant traite les images comme opaques. Le composant possède par défaut un arrière-plan transparent. Par conséquent, pour la rendre opaque, définissez la `background-color` propriété CSS sur `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> Spécifie le format d’image utilisé par le composant pour charger des images à partir d’Image Server. Si le format spécifié se termine par « -alpha », le composant effectue le rendu des images sous forme de contenu transparent ; Pour tous les autres formats d’image, le composant traite les images comme étant opaques. Le composant possède par défaut un arrière-plan transparent. Par conséquent, pour rendre opaque, affectez à la propriété CSS la couleur d’arrière-plan souhaitée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
