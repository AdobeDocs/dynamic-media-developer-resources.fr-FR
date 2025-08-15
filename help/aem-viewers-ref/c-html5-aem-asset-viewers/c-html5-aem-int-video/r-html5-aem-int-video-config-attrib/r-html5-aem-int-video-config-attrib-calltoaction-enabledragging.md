---
title: CallToAction.enabledragging
description: Attribut Configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 3%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

Attribut Configuration pour la visionneuse de vidéos interactives.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`Valeur de surglissement`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Permet ou désactive la possibilité pour un utilisateur de faire défiler les vignettes à l’aide d’une souris ou à l’aide de gestes tactiles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Valeur de surglissement </span> </span> </p> </td> 
   <td colname="col2"> <p> Est compris dans la <span class="codeph"> plage 0-1 </span> et est une valeur de pourcentage pour le mouvement dans la mauvaise direction de la vitesse réelle. </p> <p>S’il est défini sur <span class="codeph"> 1 </span>, il se déplace avec la souris. </p> <p>S’il est défini sur <span class="codeph"> 0 </span>, il ne vous permet pas d’aller dans la mauvaise direction. </p> </td> 
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
