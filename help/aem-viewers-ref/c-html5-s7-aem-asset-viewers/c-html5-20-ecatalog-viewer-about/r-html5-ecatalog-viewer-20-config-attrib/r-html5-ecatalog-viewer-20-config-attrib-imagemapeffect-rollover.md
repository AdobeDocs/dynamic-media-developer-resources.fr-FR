---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 5%

---


# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Indique le moment d’affichage du panneau d’informations. </p> <p>Si elle est définie sur <span class="codeph"> 1</span>, le panneau d’informations s’affiche lorsque la souris entre dans la zone de zone de zone cliquable (dans le cas où la zone de l’image n’est pas vide, attribut <span class="codeph"> rollover_key</span>). </p> <p>Si le paramètre est défini sur <span class="codeph"> 0</span>, le panneau d’informations est déclenché lorsque l’utilisateur clique sur la zone cliquable (si la zone cliquable comporte un attribut <span class="codeph"> rollover_key</span> non vide et un attribut <span class="codeph"> href</span> vide). </p> <p> Ignorée sur les périphériques tactiles, y compris les systèmes de bureau tactiles, et définie automatiquement sur <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-ccfedc2da28f412a86d03f390db92b4b}

Facultatif.

## Par défaut {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Exemple {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
