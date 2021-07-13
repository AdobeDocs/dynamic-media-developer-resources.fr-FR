---
description: Attribut de configuration de la visionneuse de vidéos interactives.
solution: Experience Manager
title: CallToAction.direction
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéos interactives
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# CallToAction.direction{#calltoaction-direction}

Attribut de configuration de la visionneuse de vidéos interactives.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Indique la manière dont les miniatures sont remplies dans la vue. </p> <p>Définissez cette variable sur <span class="codeph"> gauche </span> pour définir l’ordre de remplissage de gauche à droite. </p> <p>Défini sur <span class="codeph"> droite </span> inverse l’ordre de sorte que la vue soit remplie de droite à gauche, de haut en bas. </p> <p>Définissez cette variable sur <span class="codeph"> auto </span> pour que le composant applique le mode approprié lorsque le paramètre régional est défini sur <span class="codeph"> "ja" </span>; sinon, <span class="codeph"> gauche </span> est utilisé. </p> </td> 
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
