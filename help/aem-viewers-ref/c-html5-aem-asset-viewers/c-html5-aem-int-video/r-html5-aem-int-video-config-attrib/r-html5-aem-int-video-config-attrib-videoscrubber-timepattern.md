---
title: VideoScrubber.timepattern
description: Attribut de configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
TQID: 'https://experienceleague.adobe.com/ZNw6n5Zokz-s696GvaLkQJY-fAT-JoNafyLzpztZqos'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Attribut de configuration pour la visionneuse de vidéos interactives.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h :]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Définit le motif du temps affiché dans la bulle de temps, où <span class="codeph"> h</span> représente les heures, <span class="codeph"> m</span> les minutes et <span class="codeph"> s</span> les secondes. </p> <p>Le nombre de lettres utilisé pour chaque unité de temps détermine le nombre de chiffres à afficher pour l’unité. Si le nombre ne peut pas tenir dans les chiffres donnés, la valeur équivalente est affichée dans l’unité suivante. </p> <p>Par exemple, si la durée actuelle du film est de 67 minutes et 5 secondes, un modèle temporel de <span class="codeph"> m:ss</span> s’affiche à 67:05. La même heure est affichée sous la forme 1:07:5 si le modèle temporel est <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
