---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: InteractiveSwatches.maxloadradius
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
uuid: 12391b8b-532f-4e68-ad60-4dbcc86d9e58
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéos interactives
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---


# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Attribut de configuration pour la visionneuse de vidéos interactive.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le comportement de préchargement du composant. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> -1</span>, toutes les nuances sont chargées simultanément lorsque le composant est initialisé ou que la ressource est modifiée. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> 0</span>, seules les nuances visibles sont chargées. </p> <p>Définissez sur <span class="codeph"><span class="varname"> preloadnbr</span></span> pour définir le nombre de lignes/colonnes invisibles autour de la zone visible qui sont préchargées. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

