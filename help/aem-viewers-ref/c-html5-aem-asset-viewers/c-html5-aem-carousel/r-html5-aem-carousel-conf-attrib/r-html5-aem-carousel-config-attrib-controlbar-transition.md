---
title: ControlBar.transition
description: Attribut de configuration de la visionneuse de carrousel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# ControlBar.transition{#controlbar-transition}

Attribut de configuration de la visionneuse de carrousel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Indique le type d’effet utilisé pour afficher ou masquer la barre de contrôle et son contenu. </p> <p>Définissez cette variable sur <span class="codeph"> none</span> pour l’affichage/le masquage instantanés. </p> <p>Définissez cette variable sur <span class="codeph"> fondu </span> pour fournir un effet de fondu progressif en entrée/sortie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la durée en secondes entre le dernier événement de souris/touche enregistré par la barre de contrôle et la barre de contrôle de l’heure se masque. </p> <p>Si elle est définie sur <span class="codeph"> -1</span>, le composant ne déclenche jamais son effet de masquage automatique et reste donc toujours visible à l’écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> Définit la durée de l’animation de fondu en entrée/sortie en secondes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif. Cette commande est ignorée sur les périphériques tactiles pour lesquels le masquage automatique de la barre de contrôle est désactivé.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
