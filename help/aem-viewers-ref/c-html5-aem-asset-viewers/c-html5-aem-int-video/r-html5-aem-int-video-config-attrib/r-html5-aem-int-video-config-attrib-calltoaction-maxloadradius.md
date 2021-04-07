---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
solution: Experience Manager
title: CallToAction.maxloadradius
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéos interactives
role: Développeur, Professionnel
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Attribut de configuration pour la visionneuse de vidéos interactive.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le comportement de préchargement du composant. </p> <p>Lorsque cette propriété est définie sur <span class="codeph"> -1</span>, toutes les miniatures sont chargées simultanément lorsque le composant est initialisé ou que la ressource est modifiée. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> 0</span>, seules les vignettes visibles sont chargées. </p> <p>Définissez sur <span class="codeph"><span class="varname"> preloadnbr</span></span> pour définir le nombre de lignes/colonnes invisibles autour de la zone visible qui sont préchargées. </p> </td> 
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
