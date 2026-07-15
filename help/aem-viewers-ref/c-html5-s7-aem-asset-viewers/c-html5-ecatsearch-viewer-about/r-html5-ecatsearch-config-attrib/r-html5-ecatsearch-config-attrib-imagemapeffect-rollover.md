---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
TQID: 'https://experienceleague.adobe.com/V5KPk6tOhMcCUtL7iraaeBNt4xp81Uo7FTpT-1Z44ks'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Indique quand afficher le panneau d’informations. </p> <p>Si cette valeur est définie sur <span class="codeph"> 1</span>, le panneau d’informations s’affiche lorsque la souris entre dans la zone cliquable (si la zone cliquable comporte un attribut rollover_key</span> <span class="codeph"> non vide). </p> <p>Si cette valeur est définie sur <span class="codeph"> 0</span>, le panneau d’informations est déclenché lorsque la zone cliquable est sélectionnée (si la zone cliquable comporte un attribut rollover_key</span> <span class="codeph"> non vide et un attribut href</span> <span class="codeph"> vide). </p> <p> Ignoré sur les appareils tactiles, y compris les ordinateurs de bureau tactiles, et est automatiquement défini sur <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-ccfedc2da28f412a86d03f390db92b4b}

Facultatif.

## Par défaut {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Exemple {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]

