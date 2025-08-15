---
title: ControlBar.transition
description: Attribut de configuration pour la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 950b1230-5c4b-4222-87e2-d069287fc3ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Attribut de configuration pour la visionneuse Video360.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`Durée de masquage du`*[, *`délai`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Aucun|fondu</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>N’utilisez <span class="codeph"> aucun pour l’affichage</span> instantané et le masquage. Utilisez <span class="codeph"> le fondu</span> pour obtenir un effet de fondu entrant et sortant progressif. </p> <p>Le fondu n’est pas pris en charge par Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Délai de masquage</span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie le temps en secondes entre le dernier événement souris/tactile enregistré par la barre de contrôle et le masquage de la barre de contrôle de l’heure. </p> <p> S’il est défini sur <span class="codeph"> -1</span>, le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> durée</span> </span> </p> </td> 
   <td colname="col2"> <p>Définit la durée en secondes de l’animation de fondu entrant et sortant. </p> </td> 
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
