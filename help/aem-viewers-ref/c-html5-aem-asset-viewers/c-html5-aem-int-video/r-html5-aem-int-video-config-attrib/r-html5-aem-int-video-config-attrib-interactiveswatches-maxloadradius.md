---
title: InteractiveSwatches.maxloadradius
description: Attribut Configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 4%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Attribut Configuration pour la visionneuse de vidéos interactives.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie le comportement de préchargement du composant. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> -1</span> , toutes les nuances sont chargées simultanément lorsque le composant est initialisé ou que l’actif est modifié. </p> <p>Lorsque la valeur est 0<span class="codeph"></span>, seules les échantillons visibles sont chargés. </p> <p>Définissez sur <span class="codeph"><span class="varname"> preloadnbr</span></span> pour définir combien de lignes/colonnes invisibles autour de la zone visible sont préchargées. </p> </td> 
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
