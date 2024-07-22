---
title: InteractiveSwatches.textpos
description: Attribut de configuration de la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 875d36cc-7372-454e-9a04-32492a2e558e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# InteractiveSwatches.textpos{#interactiveswatches-textpos}

Attribut de configuration de la visionneuse de vidéos interactives.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]textpos=bottom|top|left|right|none|tooltip`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom|top|left|right|none|tooltip</span> </p> </td> 
   <td colname="col2"> <p> Indique l’endroit où le libellé est tracé par rapport à l’image d’échantillon. En d’autres termes, le libellé est centré à l’emplacement spécifié par rapport à la miniature. </p> <p>Lorsque <span class="codeph"> tooltip</span> est spécifié, le texte du libellé s’affiche sous la forme d’une info-bulle flottante sur l’image miniature. </p> <p>Définissez cette variable sur <span class="codeph"> none</span> pour désactiver l’étiquette. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`bottom`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
textpos=top
```
