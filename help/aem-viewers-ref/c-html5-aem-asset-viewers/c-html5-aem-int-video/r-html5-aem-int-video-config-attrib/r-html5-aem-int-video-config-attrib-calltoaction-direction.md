---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: CallToAction.direction
solution: Experience Manager
title: CallToAction.direction
topic: Dynamic media
uuid: fe182e8f-696d-4515-afdb-49964a374dae
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---


# CallToAction.direction{#calltoaction-direction}

Attribut de configuration pour la visionneuse de vidéos interactive.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Indique la façon dont les miniatures remplissent la vue. </p> <p>Définissez sur <span class="codeph"> left </span> pour définir l’ordre de remplissage de gauche à droite. </p> <p>La valeur <span class="codeph"> droite </span> inverse l’ordre de manière à ce que la vue soit remplie de droite à gauche, de haut en bas. </p> <p>Définissez cette variable sur <span class="codeph"> auto </span> pour que le composant applique le bon mode lorsque le paramètre régional est défini sur <span class="codeph"> "ja" </span>; sinon, <span class="codeph"> left </span> est utilisé. </p> </td> 
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

