---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: CallToAction.enabledragging
solution: Experience Manager
title: CallToAction.enabledragging
topic: Dynamic media
uuid: efb272b5-e30e-44d5-9dec-0529b1074ed2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.enabledragging{#calltoaction-enabledragging}

Attribut de configuration pour la visionneuse de vidéos interactive.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Active ou désactive la possibilité pour un utilisateur de faire défiler les miniatures avec la souris ou à l’aide de mouvements tactiles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue </span></span> </p> </td> 
   <td colname="col2"> <p> Est dans la plage <span class="codeph"> 0-1 </span> et c'est une valeur de pourcentage pour le mouvement dans la mauvaise direction de la vitesse réelle. </p> <p>Si la valeur est <span class="codeph"> 1, </span> il bouge avec la souris. </p> <p>Si la valeur est <span class="codeph"> 0, </span> cela ne vous permet pas de vous diriger dans la mauvaise direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

