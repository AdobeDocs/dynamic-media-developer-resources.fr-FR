---
description: Attribut de configuration pour la visionneuse de carrousel.
seo-description: Attribut de configuration pour la visionneuse de carrousel.
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.autoplay{#carouselview-autoplay}

Attribut de configuration pour la visionneuse de carrousel.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,durée][,direction]</span> </p> </td> 
   <td colname="col2"> <p> Spécifie l’activation/la désactivation, la durée d’affichage de chaque bannière dans le carrousel et la direction de la boucle automatique. </p> <p>Définissez cette valeur sur <span class="codeph"> 0</span> pour désactiver la boucle automatique. </p> <p>Définissez <span class="codeph"> 1</span> sur la boucle automatique avec la durée de  du en secondes contrôlée par la durée <span class="codeph"> de</span>la boucle. </p> <p>La direction de la boucle automatique est contrôlée avec la <span class="codeph"> direction</span>. La <span class="codeph"> direction</span> se situe entre <span class="codeph"> 1</span> droite à gauche et <span class="codeph"> 0</span> gauche à droite. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1,9`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```

