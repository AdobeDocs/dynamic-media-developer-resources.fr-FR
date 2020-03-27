---
description: Attribut de configuration pour la visionneuse de carrousel.
seo-description: Attribut de configuration pour la visionneuse de carrousel.
seo-title: ControlBar.
solution: Experience Manager
title: ControlBar.
topic: Dynamic media
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.{#controlbar-transition}

Attribut de configuration pour la visionneuse de carrousel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohidelength`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>Définissez cette variable sur <span class="codeph"> none</span> pour un affichage/masquage instantané. </p> <p>Définissez cette option sur <span class="codeph"> Fondu</span> pour obtenir un effet de fondu progressif d’entrée/sortie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la durée, en secondes, entre le dernier de la souris/touche enregistré par la barre de contrôle et les masques de la barre de contrôle de l’heure. </p> <p>Si cette propriété est définie sur <span class="codeph"> -1</span> , le composant ne déclenche jamais son effet de masquage automatique et reste donc toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p> Définit la durée en secondes de l’animation en entrée/sortie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif. Cette commande est ignorée sur les périphériques tactiles où le masquage automatique de la barre de contrôle est désactivé.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

