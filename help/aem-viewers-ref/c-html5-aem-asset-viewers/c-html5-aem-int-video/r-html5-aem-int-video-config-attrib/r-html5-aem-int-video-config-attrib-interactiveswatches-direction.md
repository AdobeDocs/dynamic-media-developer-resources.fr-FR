---
title: InteractiveSwatches.direction
description: Attribut de configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
TQID: 'https://experienceleague.adobe.com/Rl1O2CZOwu8Fp9kNIrHIGV2Ef09ssznrrrRV5J3-Gfc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 3%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Attribut de configuration pour la visionneuse de vidéos interactives.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|gauche|droite </span> </p> </td> 
   <td colname="col2"> <p> Indique la manière dont les échantillons sont remplis dans la vue. </p> <p>Définissez sur <span class="codeph">’</span> gauche pour définir l’ordre de remplissage de gauche à droite. </p> <p>Définir sur <span class="codeph"> droite </span> inverse l'ordre de sorte que la vue soit remplie de droite à gauche, de haut en bas. </p> <p>Lorsque <span class="codeph"> paramètre de </span> automatique est défini, le composant applique le mode droit lorsque le paramètre régional est défini sur « <span class="codeph"> ja </span> » ; dans le cas contraire, <span class="codeph">’</span> de gauche est utilisé. </p> </td> 
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
