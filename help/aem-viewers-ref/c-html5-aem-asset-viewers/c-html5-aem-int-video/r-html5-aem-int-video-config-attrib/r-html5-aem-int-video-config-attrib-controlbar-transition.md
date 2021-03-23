---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
uuid: cde4a5b9-4512-41a6-84ce-9f4fc2cc0399
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéos interactives
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Attribut de configuration pour la visionneuse de vidéos interactive.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le type d'effet qui sera utilisé pour afficher/masquer la barre de contrôle et son contenu. </p> <p>Définissez sur <span class="codeph"> none</span> pour l’affichage/masquage instantané. </p> <p>Définissez ce paramètre sur <span class="codeph"> fondu</span> pour obtenir un effet de fondu progressif d’entrée/sortie. Non pris en charge sur Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie la durée en secondes entre le dernier événement souris/tactile enregistré par la barre de contrôle et la barre de contrôle temporelle se cache. Si elle est définie sur <span class="codeph"> -1</span>, le composant ne déclenche jamais son effet de masquage automatique et reste donc toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p> Définit la durée de l’animation de fondu en entrée/sortie, en secondes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

