---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
TQID: 'https://experienceleague.adobe.com/klywra9qyLFdkzwADSdRM3EvwzMJ9d2lrXSLtEViFkg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Indique quand afficher le panneau d’informations. </p> <p>Si cette valeur est définie sur <span class="codeph"> 1</span>, le panneau d’informations s’affiche lorsque la souris entre dans la zone cliquable (si la zone cliquable comporte un attribut rollover_key</span> non vide <span class="codeph">). </p> <p>Si cette valeur est définie sur <span class="codeph"> 0</span> le panneau d’informations est déclenché lorsque la zone cliquable est sélectionnée (si la zone cliquable comporte des attributs rollover_key</span> et <span class="codeph"> href</span> vides <span class="codeph"> non vides). </p> <p> Ignoré sur les appareils tactiles, y compris les ordinateurs de bureau tactiles, et est automatiquement défini sur <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-ccfedc2da28f412a86d03f390db92b4b}

Facultatif.

## Par défaut {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Exemple {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
