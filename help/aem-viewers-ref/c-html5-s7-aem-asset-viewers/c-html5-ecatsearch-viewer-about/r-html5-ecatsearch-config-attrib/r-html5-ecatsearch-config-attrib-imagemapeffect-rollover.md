---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Indique le moment d’affichage du panneau d’informations. </p> <p>Si celle-ci est définie sur <span class="codeph"> 1</span>, le panneau d’informations s’affiche lorsque la souris pénètre dans la zone de zone cliquable (dans le cas où la zone cliquable comporte un attribut <span class="codeph"> rollover_key</span> non vide). </p> <p>Si celle-ci est définie sur <span class="codeph"> 0</span>, le panneau d’informations est déclenché lorsque la zone cliquable est sélectionnée (si la zone cliquable comporte un attribut <span class="codeph"> rollover_key</span> non vide et des attributs <span class="codeph"> href</span> vides). </p> <p> Ignoré sur les périphériques tactiles, y compris les systèmes de bureau tactiles, et automatiquement défini sur <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-ccfedc2da28f412a86d03f390db92b4b}

Facultatif.

## Par défaut {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Exemple {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
