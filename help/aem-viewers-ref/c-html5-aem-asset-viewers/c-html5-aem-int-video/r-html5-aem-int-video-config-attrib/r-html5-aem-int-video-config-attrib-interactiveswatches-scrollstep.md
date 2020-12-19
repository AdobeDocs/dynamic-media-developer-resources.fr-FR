---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: InteractiveSwatches.scrollstep
solution: Experience Manager
title: InteractiveSwatches.scrollstep
topic: Dynamic media
uuid: 6f521aa4-9155-4f14-bc89-e7af24af25f0
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 8%

---


# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Attribut de configuration pour la visionneuse de vidéos interactive.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`étape`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> étape</span></span> </p> </td> 
   <td colname="col2"> <p>Indique le nombre d’échantillons à faire défiler pour chaque pression sur le bouton de défilement correspondant. </p> <p>Si la valeur spécifiée est supérieure au nombre d’échantillons interactifs visibles, chaque pression sur l’écran défile uniquement en fonction du nombre d’échantillons visibles afin d’éviter l’omission d’une nuance. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`3`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
scrollstep=1
```

