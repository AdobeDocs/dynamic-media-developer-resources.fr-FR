---
description: Attribut de configuration de la visionneuse de vidéos interactives.
solution: Experience Manager
title: CallToAction.enabledragging
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéos interactives
role: Developer,User
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 5%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

Attribut de configuration de la visionneuse de vidéos interactives.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Permet ou désactive la possibilité pour un utilisateur de faire défiler les miniatures avec la souris ou à l’aide de mouvements tactiles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Se trouve dans la plage <span class="codeph"> 0-1 </span> et il s’agit d’une valeur de pourcentage pour le mouvement dans la mauvaise direction de la vitesse réelle. </p> <p>S’il est défini sur <span class="codeph"> 1 </span>, il se déplace avec la souris. </p> <p>S’il est défini sur <span class="codeph"> 0 </span>, il ne vous permet pas de vous diriger dans la mauvaise direction. </p> </td> 
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
