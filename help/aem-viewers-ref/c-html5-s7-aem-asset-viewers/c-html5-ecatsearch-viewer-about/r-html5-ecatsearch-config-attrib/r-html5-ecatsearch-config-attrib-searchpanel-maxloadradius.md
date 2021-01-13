---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
topic: Dynamic media
uuid: 37d58c88-3d45-44d9-9f2c-d616d1077906
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 7%

---


# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Indique le comportement de préchargement du composant. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> -1</span>, toutes les miniatures sont chargées simultanément lorsque le composant est initialisé ou que la ressource change. </p> <p> Lorsqu’elle est définie sur <span class="codeph"> 0</span>, seules les vignettes visibles sont chargées. </p> <p>Définissez <span class="codeph"><span class="varname"> preloadnbr</span></span> pour définir le nombre de lignes invisibles autour de la zone visible qui sont préchargées. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-4b7952997f9240e581d21bcdb173f9af}

Facultatif.

## Par défaut {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Exemple {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
