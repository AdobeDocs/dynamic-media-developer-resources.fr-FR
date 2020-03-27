---
description: Attribut de configuration pour le lecteur vidéo360.
seo-description: Attribut de configuration pour le lecteur vidéo360.
seo-title: ControlBar.
solution: Experience Manager
title: ControlBar.
topic: Dynamic media
uuid: e8c1da96-3533-4d31-9ad3-569a87948ac6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.{#controlbar-transition}

Attribut de configuration pour le lecteur vidéo360.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohidelength`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>Utilisez <span class="codeph"> none</span> pour afficher et masquer instantanément. Utilisez le <span class="codeph"> fondu</span> pour obtenir un effet de fondu d’entrée et de sortie progressif. </p> <p>Le fondu n’est pas pris en charge dans Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p>Indique la durée, en secondes, entre le dernier tactile/souris  que la barre de contrôle s’enregistre et la barre de contrôle temporel se masque. </p> <p> S’il est défini sur <span class="codeph"> -1</span> , le composant ne déclenche jamais son effet de masquage automatique et reste toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p>Définit la durée de l’animation en fondu en entrée et en sortie, en secondes. </p> </td> 
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

