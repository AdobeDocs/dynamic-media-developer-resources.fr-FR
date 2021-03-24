---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
feature: Dynamic Media Classic, Visionneuses, SDK/API, Catalogue électronique
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Indique le comportement de préchargement du composant. </p> <p>Lorsqu’il est défini sur <span class="codeph"> -1</span>, le composant précharge toutes les images du catalogue en cas d’inactivité. </p> <p> Lorsqu'il est défini sur <span class="codeph"> 0</span>, le composant charge uniquement l'image actuellement visible, l'image précédente et l'image suivante. </p> <p>Définissez <span class="codeph"><span class="varname"> preloadnbr</span></span> pour définir le nombre de cadres invisibles autour du cadre actuellement affiché qui sont préchargés en état d’inactivité. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-4b7952997f9240e581d21bcdb173f9af}

Facultatif.

## Par défaut {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Exemple {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
