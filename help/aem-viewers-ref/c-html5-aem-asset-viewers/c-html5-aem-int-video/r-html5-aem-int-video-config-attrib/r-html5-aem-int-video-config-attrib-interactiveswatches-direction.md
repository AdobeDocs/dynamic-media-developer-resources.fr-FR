---
title: InteractiveSwatches.direction
description: Attribut Configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Attribut Configuration pour la visionneuse de vidéos interactives.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|gauche|droite </span> </p> </td> 
   <td colname="col2"> <p> Spécifie la manière dont les échantillons remplissent la vue. </p> <p>Définissez l’ordre de remplissage de gauche à <span class="codeph"> </span> droite pour définir l’ordre de remplissage de gauche à droite. </p> <p>Défini sur <span class="codeph"> droite </span> inverse l’ordre de sorte que la vue est remplie de droite à gauche, de haut en bas. </p> <p>Lorsque <span class="codeph"> auto </span> est défini, le composant applique le mode droit lorsque les paramètres régionaux sont définis sur « <span class="codeph"> ja </span>» ; sinon, <span class="codeph"> left </span> est utilisé. </p> </td> 
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
