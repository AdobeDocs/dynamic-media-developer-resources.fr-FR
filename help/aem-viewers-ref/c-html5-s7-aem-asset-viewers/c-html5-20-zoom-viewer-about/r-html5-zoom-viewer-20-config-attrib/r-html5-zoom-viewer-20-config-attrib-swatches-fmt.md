---
description: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
topic: Dynamic media
uuid: 61e6372c-bab9-4aac-a8a1-dffecc2e4903
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
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

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha`
