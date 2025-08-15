---
title: VideoTime.timepattern
description: Attribut Configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: de071adf-6c3c-4702-8950-8246b8ee459e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

Attribut Configuration pour la visionneuse de vidéos interactives.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h :]m|mm :s|ss</span> </p> </td> 
   <td colname="col2"> <p> Définit le modèle de temps affiché dans la barre de contrôle, où <span class="codeph"> h</span> représente heures, <span class="codeph"> m</span> pour minutes et <span class="codeph"> s pour secondes</span> . </p> <p>Le nombre de lettres utilisées pour chaque unité de temps détermine le nombre de chiffres à afficher pour l’unité. Si le nombre ne peut pas entrer dans les chiffres donnés, la valeur équivalente est affichée dans l’unité suivante. </p> <p>Par exemple, si la durée actuelle du film est de 67 minutes et 5 secondes, un modèle de temps de <span class="codeph"> m :ss</span> affiche 67:05. La même heure est affichée comme 1:07:5 si le modèle temporel est <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
