---
description: Attribut de configuration de la visionneuse de carrousel.
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media Classic,Visionneuses,SDK/API,Bannières de carrousel
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# CarouselView.autoplay{#carouselview-autoplay}

Attribut de configuration de la visionneuse de carrousel.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direction]</span> </p> </td> 
   <td colname="col2"> <p> Spécifie la durée d’activation/de désactivation, la durée d’affichage de chaque bannière dans le carrousel et la direction de la boucle automatique. </p> <p>Définissez cette variable sur <span class="codeph"> 0</span> pour désactiver la boucle automatique. </p> <p>Définissez <span class="codeph"> 1</span> pour activer la boucle automatique avec une durée de transition en secondes contrôlée par <span class="codeph"> durée</span>. </p> <p>La direction de la boucle automatique est contrôlée avec <span class="codeph"> direction</span>. La <span class="codeph"> direction</span> est comprise entre <span class="codeph"> 1</span> de droite à gauche et <span class="codeph"> 0</span> de gauche à droite. </p> </td> 
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
