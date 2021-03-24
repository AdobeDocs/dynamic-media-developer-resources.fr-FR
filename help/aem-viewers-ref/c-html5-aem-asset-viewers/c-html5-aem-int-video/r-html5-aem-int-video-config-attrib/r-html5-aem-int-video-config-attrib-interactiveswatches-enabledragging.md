---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
solution: Experience Manager
title: InteractiveSwatches.enabledragging
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéos interactives
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---


# InteractiveSwatches.enabledragging{#interactiveswatches-enabledragging}

Attribut de configuration pour la visionneuse de vidéos interactive.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Active ou désactive la possibilité pour un utilisateur de faire défiler les échantillons avec la souris ou en utilisant des mouvements tactiles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Se trouve dans la plage <span class="codeph"> 0-1 </span> et représente un pourcentage pour le mouvement dans la mauvaise direction de la vitesse réelle. </p> <p>Si elle est définie sur <span class="codeph"> 1 </span>, elle se déplace avec la souris. </p> <p>Si la valeur est <span class="codeph"> 0 </span>, cela ne vous permet pas de vous diriger dans la mauvaise direction. </p> </td> 
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

