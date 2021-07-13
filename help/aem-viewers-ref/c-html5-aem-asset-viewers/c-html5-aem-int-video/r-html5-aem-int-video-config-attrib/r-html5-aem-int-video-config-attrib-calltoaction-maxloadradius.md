---
description: Attribut de configuration de la visionneuse de vidéos interactives.
solution: Experience Manager
title: CallToAction.maxloadradius
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéos interactives
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Attribut de configuration de la visionneuse de vidéos interactives.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le comportement de préchargement du composant. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> -1</span>, toutes les miniatures sont chargées simultanément lorsque le composant est initialisé ou que la ressource est modifiée. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> 0</span>, seules les miniatures visibles sont chargées. </p> <p>Définissez cette variable sur <span class="codeph"><span class="varname"> preloadnbr</span></span> pour définir le nombre de lignes/colonnes invisibles autour de la zone visible qui sont préchargées. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`-1`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
