---
description: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
topic: Dynamic media
uuid: 76a2793e-bda0-408c-b09e-767a3ef27986
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Indique le format d’image utilisé par le composant pour le chargement des images à partir du serveur Image Server. Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images sous forme de contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. Notez que le composant possède par défaut un arrière-plan blanc. Par conséquent, pour rendre l’arrière-plan transparent, définissez la propriété CSS <span class="codeph"> Background-color</span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt-png-alpha`
