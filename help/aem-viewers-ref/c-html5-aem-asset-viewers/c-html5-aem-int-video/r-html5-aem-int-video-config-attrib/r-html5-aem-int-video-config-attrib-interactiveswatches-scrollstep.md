---
title: InteractiveSwatches.scrollstep
description: Attribut de configuration de la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Attribut de configuration de la visionneuse de vidéos interactives.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`step`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p>Indique le nombre d’échantillons à faire défiler pour chaque appui du bouton de défilement correspondant. </p> <p>Si la valeur spécifiée est supérieure au nombre d’échantillons interactifs visibles, chaque appui fait défiler uniquement le nombre d’échantillons visibles pour éviter l’omission d’un échantillon. </p> </td> 
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
