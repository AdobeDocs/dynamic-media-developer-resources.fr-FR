---
title: ControlBar.transition
description: Attribut de configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Attribut de configuration pour la visionneuse de vidéos interactives.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|fondu</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le type d'effet utilisé pour afficher/masquer la barre de contrôle et son contenu. </p> <p>Définissez-le sur <span class="codeph"> aucun</span> par exemple pour afficher/masquer instantanément. </p> <p>Définissez cette option sur <span class="codeph"> fondu</span> afin de fournir un effet de fondu d’entrée/sortie progressif. Non pris en charge sur Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le temps, en secondes, qui s’écoule entre le dernier événement souris/toucher enregistré par la barre de contrôle et le masquage de cette dernière. Si cette valeur est définie sur <span class="codeph"> -1</span> le composant ne déclenche jamais son effet de masquage automatique et reste donc toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p> Définit la durée de l’animation d’entrée/sortie en fondu, en secondes. </p> </td> 
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
