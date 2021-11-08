---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Indique le moment d’affichage du panneau d’informations. </p> <p>Si la variable est définie sur <span class="codeph"> 1</span>, le panneau d’informations s’affiche lorsque la souris pénètre dans la zone cliquable (dans le cas où la zone cliquable n’est pas vide, <span class="codeph"> rollover_key</span> ). </p> <p>Si la variable est définie sur <span class="codeph"> 0</span> le panneau d’informations est déclenché lorsque la zone cliquable est sélectionnée (si la zone cliquable est non vide). <span class="codeph"> rollover_key</span> et vide <span class="codeph"> href</span> Attributs). </p> <p> Ignoré sur les périphériques tactiles, y compris les systèmes de bureau tactiles, et est automatiquement défini sur <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-ccfedc2da28f412a86d03f390db92b4b}

Facultatif.

## Par défaut {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Exemple {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
