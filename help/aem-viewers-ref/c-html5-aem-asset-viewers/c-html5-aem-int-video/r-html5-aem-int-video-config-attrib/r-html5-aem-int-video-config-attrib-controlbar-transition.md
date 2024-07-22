---
title: ControlBar.transition
description: Attribut de configuration de la visionneuse de vidéos interactives.
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

Attribut de configuration de la visionneuse de vidéos interactives.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher/masquer la barre de contrôle et son contenu. </p> <p>Définissez cette variable sur <span class="codeph"> none</span> pour l’affichage/le masquage instantanés. </p> <p>Définissez cette variable sur <span class="codeph"> fondu </span> pour fournir un effet de fondu progressif en entrée/sortie. Non pris en charge sur Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la durée en secondes entre le dernier événement de souris/touche enregistré par la barre de contrôle et la barre de contrôle de l’heure se masque. Si elle est définie sur <span class="codeph"> -1</span>, le composant ne déclenche jamais son effet de masquage automatique et reste donc toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
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
