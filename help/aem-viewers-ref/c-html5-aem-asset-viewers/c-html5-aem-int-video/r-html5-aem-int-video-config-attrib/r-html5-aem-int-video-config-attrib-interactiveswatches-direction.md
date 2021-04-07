---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
solution: Experience Manager
title: InteractiveSwatches.direction
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéos interactives
role: Développeur, Professionnel
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Attribut de configuration pour la visionneuse de vidéos interactive.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Indique la façon dont les nuances remplissent la vue. </p> <p>Définissez sur <span class="codeph"> left </span> pour définir l’ordre de remplissage de gauche à droite. </p> <p>La valeur <span class="codeph"> droite </span> inverse l’ordre de manière à ce que la vue soit remplie de droite à gauche, de haut en bas. </p> <p>Lorsque <span class="codeph"> auto </span> est défini, le composant applique le mode droit lorsque le paramètre régional est défini sur " <span class="codeph"> ja </span>"; sinon, <span class="codeph"> left </span> est utilisé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
