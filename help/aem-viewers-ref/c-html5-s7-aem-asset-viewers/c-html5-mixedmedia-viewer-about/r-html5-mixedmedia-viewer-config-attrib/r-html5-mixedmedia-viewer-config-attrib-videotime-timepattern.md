---
description: 'null'
seo-description: 'null'
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: 57c86b63-7495-4f6f-bd30-8c4ebf017e36
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Définit le modèle de la durée affichée dans la barre de contrôle, où <span class="codeph"> h</span> est heures, <span class="codeph"> m</span> est minutes et s <span class="codeph"></span> est secondes. </p> <p>Le nombre de lettres utilisé pour chaque unité de temps détermine le nombre de chiffres à afficher pour l’unité. Si le nombre ne peut pas tenir dans les chiffres donnés, la valeur équivalente est affichée dans l’unité suivante. </p> <p>Par exemple, si l’heure actuelle du film est de 67 minutes et de 5 secondes, le modèle d’heure <span class="codeph"> m:ss</span> est de 67:05. La même heure est affichée sous la forme 1:07:5 si le modèle d’heure donné est <span class="codeph"> :mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
