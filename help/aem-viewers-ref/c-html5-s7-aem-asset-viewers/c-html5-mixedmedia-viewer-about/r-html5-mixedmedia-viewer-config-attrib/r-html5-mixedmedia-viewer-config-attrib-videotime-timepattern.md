---
title: VideoTime.timepattern
description: VideoTime.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0c79b3e2-ac5a-43c3-ac52-8240e7ed3cc1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h :]m|mm :s|ss</span> </p> </td> 
   <td colname="col2"> <p> Définit le modèle de temps affiché dans la barre de contrôle, où <span class="codeph"> h</span> est heures, <span class="codeph"> m</span> est minutes et <span class="codeph"> s</span> est secondes. </p> <p>Le nombre de lettres utilisées pour chaque unité de temps détermine le nombre de chiffres à afficher pour l’unité. Si le nombre ne peut pas entrer dans les chiffres donnés, la valeur équivalente est affichée dans l’unité suivante. </p> <p>Par exemple, si la durée actuelle du film est de 67 minutes et 5 secondes, le modèle <span class="codeph"> de temps m :ss</span> affiche 67:05. La même heure est affichée comme 1:07:5 si le modèle temporel donné est <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
