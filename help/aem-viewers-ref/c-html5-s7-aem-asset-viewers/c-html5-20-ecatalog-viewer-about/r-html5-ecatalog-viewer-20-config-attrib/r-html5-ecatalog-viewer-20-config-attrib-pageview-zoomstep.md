---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic, Visionneuses, SDK/API, Catalogue électronique
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 6%

---


# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *``*[, *`pas à pas`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> étape</span></span> </p> </td> 
   <td colname="col2"> <p> Configure le nombre d’actions de zoom avant et d’zoom arrière nécessaires pour augmenter ou diminuer la résolution d’un facteur de deux. La modification de résolution pour chaque action de zoom est de 2^1 par étape. Définissez ce paramètre sur <span class="codeph"> 0</span> pour effectuer un zoom en résolution maximale avec une seule action de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limiter</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la résolution de zoom maximale par rapport à l’image de résolution complète. La valeur par défaut est <span class="codeph"> 1.0</span>, ce qui n’autorise pas le zoom au-delà de la résolution maximale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-636d35a4791447039f1902973f568320}

Facultatif.

## Par défaut {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Exemple {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
