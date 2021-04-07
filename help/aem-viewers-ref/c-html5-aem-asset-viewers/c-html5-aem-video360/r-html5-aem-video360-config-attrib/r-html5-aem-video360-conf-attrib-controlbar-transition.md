---
description: Attribut de configuration pour la visionneuse Video360.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: 950b1230-5c4b-4222-87e2-d069287fc3ff
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Attribut de configuration pour la visionneuse Video360.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>Utilisez <span class="codeph"> none</span> pour afficher et masquer instantanément. Utilisez <span class="codeph"> fondu</span> pour obtenir un effet de fondu progressif et de fondu. </p> <p>Le fondu n’est pas pris en charge dans Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique la durée, en secondes, entre le dernier événement souris/tactile que la barre de contrôle enregistre et la barre de contrôle temporelle masque. </p> <p> Si elle est définie sur <span class="codeph"> -1</span>, le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée</span> </span> </p> </td> 
   <td colname="col2"> <p>Définit la durée de l’animation en fondu et en fondu, en secondes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
