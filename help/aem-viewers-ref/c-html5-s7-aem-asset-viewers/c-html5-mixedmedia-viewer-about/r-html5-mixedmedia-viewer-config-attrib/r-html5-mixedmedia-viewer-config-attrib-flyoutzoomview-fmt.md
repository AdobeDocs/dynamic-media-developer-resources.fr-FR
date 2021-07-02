---
description: Indique le format d’image que le composant utilise pour charger les images à partir du serveur d’images.
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Indique le format d’image que le composant utilise pour charger les images à partir du serveur d’images.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images en tant que contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. </p> <p>Notez que le composant a par défaut un arrière-plan blanc. Par conséquent, pour le rendre complètement transparent, définissez la propriété CSS <span class="codeph"> background-color</span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
