---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic,Visionneuses,SDK/API,Fenêtre déroulante
role: Developer,User
exl-id: b02f033d-be84-4cd0-b4bb-3ae9e424680c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le comportement de préchargement du composant. Lorsqu’elle est définie sur <span class="codeph"> -1</span>, tous les échantillons sont chargés simultanément lorsque le composant est initialisé ou que la ressource est modifiée. Lorsqu’elle est définie sur <span class="codeph"> 0</span>, seuls les échantillons visibles sont chargés. </p> <p><span class="codeph"> <span class="varname"> </span></span> preloadnbrdéfinit le nombre de lignes/colonnes invisibles autour de la zone visible qui seront préchargées. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`1`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`maxloadradius=-1`
