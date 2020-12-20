---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: InteractiveSwatches.direction
solution: Experience Manager
title: InteractiveSwatches.direction
topic: Dynamic media
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 4%

---


# InteractiveSwatches.direction{#interactiveswatches-direction}

Attribut de configuration pour la visionneuse de vidéos interactive.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Indique la façon dont les nuances remplissent la vue. </p> <p>Définissez sur <span class="codeph"> left </span> pour définir l’ordre de remplissage de gauche à droite. </p> <p>La valeur <span class="codeph"> droite </span> inverse l’ordre de manière à ce que la vue soit remplie de droite à gauche, de haut en bas. </p> <p>Lorsque <span class="codeph"> auto </span> est défini, le composant applique le mode droit lorsque le paramètre régional est défini sur " <span class="codeph"> ja </span>"; sinon, <span class="codeph"> left </span> est utilisé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```

