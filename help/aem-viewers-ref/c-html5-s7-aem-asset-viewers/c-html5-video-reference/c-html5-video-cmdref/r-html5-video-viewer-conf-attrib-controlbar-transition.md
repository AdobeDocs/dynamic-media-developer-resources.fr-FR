---
title: ControlBar.transition
description: Attribut de configuration pour la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Attribut de configuration pour la visionneuse de vidéos.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>Utilisez <span class="codeph"> none</span> pour l’affichage et le masquage instantanés. Utilisez <span class="codeph"> fondu</span> pour créer un effet de fondu progressif dans et de fondu. </p> <p>Le fondu n’est pas pris en charge sur Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique la durée en secondes entre le dernier événement de souris/touche enregistré par la barre de contrôle et la durée masquée par la barre de contrôle. </p> <p> S’il est défini sur <span class="codeph"> -1</span>, le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Définit la durée en secondes de l’animation de fondu et de fondu. </p> </td> 
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
